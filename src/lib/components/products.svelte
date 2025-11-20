<section class="products-section">
	<div class="container">
		<h2 class="section-title">Sulthoni Collection</h2>
		<p class="section-subtitle">Meticulously crafted pieces inspired by Saudi nobility</p>
		
		<div class="products-grid">
			{#each products as product (product.id)}
				<div class="product-card">
					<div class="product-image">
						<img 
							src={product.image || "/placeholder.svg"}
							alt={product.name}
						/>
					</div>
					<div class="product-info">
						<h3>{product.name}</h3>
						<p class="product-material">{product.material}</p>
						<ul class="product-features">
							{#each product.features as feature}
								<li>{feature}</li>
							{/each}
						</ul>
						<button onclick={() => viewDetails(product)}>View Details</button>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<script lang="ts">
	interface Props {
		viewDetails: (product: any) => void;
	}

	let { viewDetails }: Props = $props();

	const products = [
		{
			id: 1,
			name: "Sulthoni Classic",
			material: "Premium Polyester-Spandex",
			image: "/placeholder.svg?height=600&width=500",
			features: ["Precision-cut collar", "Hidden zipper", "Silky drape"]
		},
		{
			id: 2,
			name: "Sulthoni Refined",
			material: "Premium Polyester-Spandex",
			image: "/placeholder.svg?height=600&width=500",
			features: ["Reinforced cuff", "Minimal seaming", "Premium finish"]
		},
		{
			id: 3,
			name: "Sulthoni Prestige",
			material: "Premium Polyester-Spandex",
			image: "/placeholder.svg?height=600&width=500",
			features: ["Detailed embroidery", "Precision tailoring", "Elevated elegance"]
		}
	];
</script>

<style>
	.products-section {
		background: linear-gradient(135deg, hsl(35 56% 95%) 0%, hsl(35 46% 97%) 100%);
		padding: 80px 20px;
	}

	.container {
		max-width: 1200px;
		margin: 0 auto;
	}

	.section-title {
		font-size: 2.5rem;
		font-weight: 400;
		color: hsl(20 30% 20%);
		margin-bottom: 12px;
		text-align: center;
		font-family: ui-serif, Georgia, serif;
		letter-spacing: -1px;
	}

	.section-subtitle {
		text-align: center;
		color: hsl(20 15% 35%);
		font-size: 1.1rem;
		margin-bottom: 60px;
		line-height: 1.6;
	}

	.products-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 40px;
	}

	.product-card {
		background: white;
		border-radius: 2px;
		overflow: hidden;
		transition: all 0.3s ease;
		box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
	}

	.product-card:hover {
		transform: translateY(-4px);
		box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
	}

	.product-image {
		width: 100%;
		height: 300px;
		overflow: hidden;
		background-color: hsl(35 56% 92%);
	}

	.product-image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.product-info {
		padding: 32px 24px;
	}

	.product-info h3 {
		font-size: 1.3rem;
		color: hsl(20 30% 20%);
		margin-bottom: 8px;
		font-family: ui-serif, Georgia, serif;
		font-weight: 400;
	}

	.product-material {
		color: hsl(35 80% 50%);
		font-size: 0.85rem;
		font-weight: 500;
		text-transform: uppercase;
		letter-spacing: 1px;
		margin-bottom: 16px;
	}

	.product-features {
		list-style: none;
		padding: 0;
		margin: 0 0 24px 0;
	}

	.product-features li {
		color: hsl(20 15% 35%);
		font-size: 0.9rem;
		line-height: 1.6;
		padding-left: 20px;
		position: relative;
	}

	.product-features li:before {
		content: "•";
		color: hsl(35 80% 60%);
		position: absolute;
		left: 0;
		font-weight: bold;
	}

	@media (max-width: 768px) {
		.products-grid {
			grid-template-columns: 1fr;
			gap: 30px;
		}

		.section-title {
			font-size: 1.75rem;
		}

		.products-section {
			padding: 60px 20px;
		}
	}
</style>
