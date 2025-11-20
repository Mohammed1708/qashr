<section class="about-section">
	<div class="container">
		<h2 class="section-title">About Qashr.id</h2>
		<div class="about-content">
			<div class="about-text">
				<h3>Our Story</h3>
				<p>
					Qashr.id draws inspiration from the timeless elegance of Saudi nobility, merging authentic Arabian aesthetics with contemporary functionality. We believe that modest fashion should never compromise on quality, comfort, or sophistication.
				</p>
				<p>
					Each Sulthoni piece is meticulously crafted to honor both tradition and modernity—designed for the modern noble man who values craftsmanship, elegance, and the ease of everyday wear.
				</p>
			</div>
			<div class="values-grid">
				<div class="value-item">
					<div class="value-icon">✨</div>
					<h4>Premium Quality</h4>
					<p>Polyester-spandex blend ensures durability and silky softness</p>
				</div>
				<div class="value-item">
					<div class="value-icon">🎯</div>
					<h4>Precision Crafting</h4>
					<p>Every detail meticulously tailored for perfect fit and finish</p>
				</div>
				<div class="value-item">
					<div class="value-icon">🕌</div>
					<h4>Versatile Elegance</h4>
					<p>Perfect for daily wear, formal occasions, and religious observances</p>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.about-section {
		background-color: hsl(0 0% 100%);
		padding: 80px 20px;
	}

	.container {
		max-width: 1000px;
		margin: 0 auto;
	}

	.section-title {
		font-size: 2.5rem;
		font-weight: 400;
		color: hsl(20 30% 20%);
		margin-bottom: 60px;
		text-align: center;
		font-family: ui-serif, Georgia, serif;
		letter-spacing: -1px;
	}

	.about-content {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 60px;
	}

	.about-text h3 {
		font-size: 1.5rem;
		color: hsl(20 30% 20%);
		margin-bottom: 20px;
		font-family: ui-serif, Georgia, serif;
		font-weight: 400;
	}

	.about-text p {
		color: hsl(20 15% 35%);
		line-height: 1.8;
		margin-bottom: 20px;
		font-size: 1rem;
	}

	.values-grid {
		display: flex;
		flex-direction: column;
		gap: 24px;
	}

	.value-item {
		padding: 24px;
		background-color: hsl(35 56% 95%);
		border-left: 3px solid hsl(35 80% 60%);
		border-radius: 2px;
	}

	.value-icon {
		font-size: 1.75rem;
		margin-bottom: 12px;
		display: block;
	}

	.value-item h4 {
		font-size: 1.1rem;
		color: hsl(20 30% 20%);
		margin-bottom: 8px;
		font-weight: 500;
	}

	.value-item p {
		color: hsl(20 15% 35%);
		font-size: 0.95rem;
		line-height: 1.6;
		margin: 0;
	}

	@media (max-width: 768px) {
		.about-content {
			grid-template-columns: 1fr;
			gap: 40px;
		}

		.section-title {
			font-size: 1.75rem;
		}

		.about-section {
			padding: 60px 20px;
		}
	}
</style>
