<section class="testimonials-section">
	<div class="container">
		<h2 class="section-title">What Our Customers Say</h2>
		<div class="testimonials-grid">
			{#each testimonials as testimonial (testimonial.id)}
				<div class="testimonial-card">
					<div class="stars">
						{'★'.repeat(5)}
					</div>
					<p class="testimonial-text">"{testimonial.text}"</p>
					<div class="testimonial-author">
						<div class="author-avatar">{testimonial.initials}</div>
						<div class="author-info">
							<h4>{testimonial.name}</h4>
							<p>{testimonial.role}</p>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<script lang="ts">
	const testimonials = [
		{
			id: 1,
			name: "Ahmad Rizki",
			role: "Jakarta",
			initials: "AR",
			text: "Mengenakan Qashr membuat saya merasa sangat anggun. Bahannya lembut tapi terasa premium, dan potongannya sangat presisi. Sempurna untuk keseharian dan acara formal."
		},
		{
			id: 2,
			name: "Malik Hassan",
			role: "Bandung",
			initials: "MH",
			text: "Kualitas yang luar biasa. Saya sudah mencoba banyak brand, tapi Sulthoni Collection menang di aspek desain dan kenyamanan. Jahitannya rapi, hidden zipper-nya fungsional."
		},
		{
			id: 3,
			name: "Fatih Yusuf",
			role: "Surabaya",
			initials: "FY",
			text: "Ini adalah representasi sempurna dari modest luxury. Desainnya elegan, tidak berlebihan, dan cocok baik untuk beribadah maupun aktivitas formal. Highly recommended!"
		}
	];
</script>

<style>
	.testimonials-section {
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
		margin-bottom: 60px;
		text-align: center;
		font-family: ui-serif, Georgia, serif;
		letter-spacing: -1px;
	}

	.testimonials-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 32px;
	}

	.testimonial-card {
		background: white;
		padding: 32px;
		border-radius: 2px;
		box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
		transition: all 0.3s ease;
	}

	.testimonial-card:hover {
		box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
		transform: translateY(-4px);
	}

	.stars {
		color: hsl(35 80% 60%);
		font-size: 1.1rem;
		margin-bottom: 16px;
		letter-spacing: 2px;
	}

	.testimonial-text {
		color: hsl(20 15% 35%);
		font-size: 0.95rem;
		line-height: 1.8;
		margin-bottom: 24px;
		font-style: italic;
	}

	.testimonial-author {
		display: flex;
		align-items: center;
		gap: 16px;
	}

	.author-avatar {
		width: 48px;
		height: 48px;
		background: linear-gradient(135deg, hsl(35 80% 60%), hsl(35 80% 50%));
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
		color: white;
		font-weight: 600;
		font-size: 0.9rem;
	}

	.author-info h4 {
		margin: 0;
		color: hsl(20 30% 20%);
		font-size: 0.95rem;
		font-weight: 500;
	}

	.author-info p {
		margin: 0;
		color: hsl(20 15% 35%);
		font-size: 0.85rem;
	}

	@media (max-width: 768px) {
		.testimonials-grid {
			grid-template-columns: 1fr;
		}

		.section-title {
			font-size: 1.75rem;
		}

		.testimonials-section {
			padding: 60px 20px;
		}
	}
</style>
