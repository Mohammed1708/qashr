<section class="advantages-section">
	<div class="container">
		<h2 class="section-title">Why Choose Qashr.id</h2>
		<div class="advantages-grid">
			{#each advantages as advantage (advantage.id)}
				<div class="advantage-card">
					<div class="advantage-icon">{advantage.icon}</div>
					<h3>{advantage.title}</h3>
					<p>{advantage.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<script lang="ts">
	const advantages = [
		{
			id: 1,
			icon: "🧵",
			title: "Premium Materials",
			description: "Polyester-spandex blend engineered for durability, comfort, and that coveted silky-soft feel"
		},
		{
			id: 2,
			icon: "✂️",
			title: "Precision Tailoring",
			description: "Every garment features meticulous cuts, reinforced cuffs, and hidden zippers for seamless elegance"
		},
		{
			id: 3,
			icon: "🌙",
			title: "Versatile Design",
			description: "Crafted for both daily elegance and religious observances—effortless transition from work to prayer"
		},
		{
			id: 4,
			icon: "👑",
			title: "Noble Aesthetic",
			description: "Inspired by Saudi nobility, capturing the essence of modest luxury and timeless sophistication"
		}
	];
</script>

<style>
	.advantages-section {
		background-color: hsl(0 0% 100%);
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
		margin-bottom: 60px;
		text-align: center;
		font-family: ui-serif, Georgia, serif;
		letter-spacing: -1px;
	}

	.advantages-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		gap: 40px;
	}

	.advantage-card {
		text-align: center;
		padding: 32px;
		border-radius: 2px;
		background: linear-gradient(135deg, hsl(35 56% 97%) 0%, hsl(35 46% 98%) 100%);
		transition: all 0.3s ease;
	}

	.advantage-card:hover {
		background: linear-gradient(135deg, hsl(35 56% 95%) 0%, hsl(35 46% 96%) 100%);
		transform: translateY(-4px);
	}

	.advantage-icon {
		font-size: 2.5rem;
		margin-bottom: 16px;
		display: block;
	}

	.advantage-card h3 {
		font-size: 1.25rem;
		color: hsl(20 30% 20%);
		margin-bottom: 12px;
		font-family: ui-serif, Georgia, serif;
		font-weight: 400;
	}

	.advantage-card p {
		color: hsl(20 15% 35%);
		font-size: 0.95rem;
		line-height: 1.7;
		margin: 0;
	}

	@media (max-width: 768px) {
		.advantages-grid {
			grid-template-columns: 1fr;
			gap: 24px;
		}

		.section-title {
			font-size: 1.75rem;
		}

		.advantages-section {
			padding: 60px 20px;
		}
	}
</style>
