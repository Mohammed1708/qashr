<script lang="ts">
	interface Product {
		id: number;
		name: string;
		material: string;
		image: string;
		features: string[];
	}

	interface Props {
		product: Product | null;
		isOpen: boolean;
		onClose: () => void;
	}

	let { product, isOpen, onClose }: Props = $props();

	function handleBackdropClick(e: MouseEvent) {
		if ((e.target as HTMLElement) === e.currentTarget) {
			onClose();
		}
	}

	function handleKeydown(e: KeyboardEvent) {
		if (e.key === 'Escape') {
			onClose();
		}
	}
</script>

{#if isOpen && product}
	<div class="modal-backdrop" role="dialog" aria-modal="true" tabindex="0" onclick={handleBackdropClick} onkeydown={handleKeydown}>
		<div class="modal-content">
			<button class="close-button" onclick={onClose} aria-label="Close modal">
				<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<line x1="18" y1="6" x2="6" y2="18"></line>
					<line x1="6" y1="6" x2="18" y2="18"></line>
				</svg>
			</button>

			<div class="modal-grid">
				<div class="modal-image-section">
					<img src={product.image || "/placeholder.svg"} alt={product.name} class="modal-image" />
				</div>

				<div class="modal-details">
					<h2 class="modal-title">{product.name}</h2>
					<p class="modal-material">{product.material}</p>
					
					<div class="modal-description">
						<p class="description-text">The {product.name} represents the pinnacle of Saudi-inspired elegance, meticulously crafted for the modern Muslim gentleman.</p>
					</div>

					<div class="features-section">
						<h3 class="features-title">Key Features</h3>
						<ul class="modal-features">
							{#each product.features as feature}
								<li>{feature}</li>
							{/each}
						</ul>
					</div>

					<div class="modal-specs">
						<h3 class="specs-title">Specifications</h3>
						<div class="spec-item">
							<span class="spec-label">Material:</span>
							<span class="spec-value">{product.material}</span>
						</div>
						<div class="spec-item">
							<span class="spec-label">Fit:</span>
							<span class="spec-value">Contemporary Tailored</span>
						</div>
						<div class="spec-item">
							<span class="spec-label">Care:</span>
							<span class="spec-value">Hand wash recommended</span>
						</div>
					</div>

					<button class="cta-button" onclick={onClose}>Back to Collection</button>
				</div>
			</div>
		</div>
	</div>
{/if}

<style>
	.modal-backdrop {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-color: rgba(0, 0, 0, 0.5);
		display: flex;
		align-items: center;
		justify-content: center;
		z-index: 1000;
		padding: 20px;
		backdrop-filter: blur(4px);
	}

	.modal-content {
		background: white;
		border-radius: 8px;
		width: 100%;
		max-width: 1000px;
		max-height: 90vh;
		overflow-y: auto;
		position: relative;
		box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
	}

	.close-button {
		position: absolute;
		top: 20px;
		right: 20px;
		background: hsl(35 56% 92%);
		border: none;
		width: 40px;
		height: 40px;
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
		cursor: pointer;
		color: hsl(20 30% 20%);
		transition: all 0.2s ease;
		z-index: 10;
	}

	.close-button:hover {
		background: hsl(35 80% 60%);
		color: white;
	}

	.modal-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 40px;
		padding: 40px;
	}

	.modal-image-section {
		display: flex;
		align-items: center;
		justify-content: center;
		background: hsl(35 56% 92%);
		border-radius: 4px;
		overflow: hidden;
		min-height: 500px;
	}

	.modal-image {
		width: 100%;
		height: 100%;
		object-fit: contain;
		padding: 20px;
	}

	.modal-details {
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		gap: 24px;
	}

	.modal-title {
		font-size: 2rem;
		font-weight: 400;
		color: hsl(20 30% 20%);
		font-family: ui-serif, Georgia, serif;
		margin: 0;
		letter-spacing: -0.5px;
	}

	.modal-material {
		color: hsl(35 80% 50%);
		font-size: 0.85rem;
		font-weight: 500;
		text-transform: uppercase;
		letter-spacing: 1.5px;
		margin: 0;
	}

	.modal-description {
		padding-top: 16px;
		border-top: 1px solid hsl(35 56% 92%);
	}

	.description-text {
		color: hsl(20 15% 35%);
		font-size: 1rem;
		line-height: 1.8;
		margin: 0;
	}

	.features-section {
		display: flex;
		flex-direction: column;
		gap: 12px;
	}

	.features-title {
		font-size: 1.1rem;
		font-weight: 500;
		color: hsl(20 30% 20%);
		margin: 0;
		font-family: ui-serif, Georgia, serif;
	}

	.modal-features {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.modal-features li {
		color: hsl(20 15% 35%);
		font-size: 0.95rem;
		line-height: 1.8;
		padding-left: 24px;
		position: relative;
	}

	.modal-features li:before {
		content: "✓";
		color: hsl(35 80% 60%);
		position: absolute;
		left: 0;
		font-weight: bold;
		font-size: 1.1rem;
	}

	.modal-specs {
		padding: 20px;
		background: hsl(35 56% 96%);
		border-radius: 4px;
	}

	.specs-title {
		font-size: 0.95rem;
		font-weight: 600;
		color: hsl(20 30% 20%);
		margin: 0 0 16px 0;
		font-family: ui-serif, Georgia, serif;
		text-transform: uppercase;
		letter-spacing: 0.5px;
	}

	.spec-item {
		display: flex;
		justify-content: space-between;
		padding: 8px 0;
		border-bottom: 1px solid hsl(35 70% 92%);
		color: hsl(20 15% 35%);
		font-size: 0.9rem;
	}

	.spec-item:last-child {
		border-bottom: none;
	}

	.spec-label {
		font-weight: 500;
	}

	.spec-value {
		color: hsl(20 20% 40%);
	}

	.cta-button {
		background: hsl(20 30% 20%);
		color: white;
		border: none;
		padding: 14px 32px;
		font-size: 1rem;
		font-weight: 500;
		border-radius: 4px;
		cursor: pointer;
		transition: all 0.3s ease;
		letter-spacing: 0.3px;
	}

	.cta-button:hover {
		background: hsl(35 80% 60%);
		transform: translateY(-2px);
	}

	@media (max-width: 768px) {
		.modal-grid {
			grid-template-columns: 1fr;
			gap: 30px;
			padding: 24px;
		}

		.modal-image-section {
			min-height: 300px;
		}

		.modal-title {
			font-size: 1.5rem;
		}

		.close-button {
			top: 12px;
			right: 12px;
		}

		.modal-content {
			max-height: 95vh;
			border-radius: 12px;
		}
	}

	@media (max-width: 480px) {
		.modal-backdrop {
			padding: 0;
		}

		.modal-content {
			border-radius: 0;
			max-height: 100vh;
		}

		.modal-grid {
			padding: 16px;
			gap: 20px;
		}

		.modal-title {
			font-size: 1.25rem;
		}

		.modal-details {
			gap: 16px;
		}
	}
</style>
