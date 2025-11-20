<script lang="ts">
	interface Props {
		onExploreClick?: () => void;
	}

	let { onExploreClick = () => {} }: Props = $props();
</script>

<section class="hero-section">
	<div class="container">
		<div class="hero-content">
			<h1 class="hero-title">Elegance of the Kingdom</h1>
			<p class="hero-subtitle">Saudi-inspired craftsmanship for the modern noble</p>
			<button class="cta-button" onclick={() => onExploreClick()}>Explore Sulthoni Collection</button>
		</div>
		<div class="hero-image">
			<img 
				src="/placeholder.svg?height=500&width=500"
				alt="Qashr.id Sulthoni Collection"
				class="garment-image"
			/>
		</div>
	</div>
</section>

<style>
	.hero-section {
		background: linear-gradient(135deg, hsl(35 56% 88%) 0%, hsl(35 46% 92%) 100%);
		min-height: 600px;
		display: flex;
		align-items: center;
		padding: 60px 20px;
	}

	.container {
		max-width: 1200px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 60px;
		align-items: center;
	}

	.hero-content {
		display: flex;
		flex-direction: column;
		gap: 24px;
	}

	.hero-title {
		font-size: clamp(2.5rem, 5vw, 4rem);
		font-weight: 400;
		color: hsl(20 30% 20%);
		line-height: 1.2;
		letter-spacing: -1px;
		font-family: ui-serif, Georgia, serif;
	}

	.hero-subtitle {
		font-size: 1.125rem;
		color: hsl(20 15% 35%);
		line-height: 1.6;
		max-width: 400px;
	}

	.cta-button {
		align-self: flex-start;
		padding: 14px 36px;
		background-color: hsl(20 30% 20%);
		color: hsl(35 56% 92%);
		border: none;
		border-radius: 4px;
		font-size: 0.95rem;
		font-weight: 500;
		letter-spacing: 0.5px;
		cursor: pointer;
		transition: all 0.3s ease;
		text-transform: uppercase;
	}

	.cta-button:hover {
		background-color: hsl(20 35% 30%);
		transform: translateY(-2px);
	}

	.hero-image {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.garment-image {
		width: 100%;
		max-width: 450px;
		height: auto;
		border-radius: 2px;
		object-fit: cover;
	}

	@media (max-width: 768px) {
		.container {
			grid-template-columns: 1fr;
			gap: 40px;
		}

		.hero-section {
			min-height: auto;
			padding: 40px 20px;
		}

		.cta-button {
			width: 100%;
		}
	}
</style>
