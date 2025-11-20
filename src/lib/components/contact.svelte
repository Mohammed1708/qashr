<script lang="ts">
	function handleSubmit(event) {
		event.preventDefault();
		const form = event.currentTarget;
		// In a real app, this would send data to a backend
		alert('Thank you for your message! We will get back to you soon.');
		form.reset();
	}
</script>

<section class="contact-section">
	<div class="container">
		<h2 class="section-title">Get In Touch</h2>
		
		<div class="contact-content">
			<div class="contact-form">
				<form onsubmit={handleSubmit}>
					<div class="form-group">
						<label for="name">Your Name</label>
						<input type="text" id="name" placeholder="Ahmad" required />
					</div>
					<div class="form-group">
						<label for="email">Email Address</label>
						<input type="email" id="email" placeholder="ahmad@example.com" required />
					</div>
					<div class="form-group">
						<label for="message">Message</label>
						<textarea id="message" placeholder="Tell us about your inquiry..." rows="5" required></textarea>
					</div>
					<button type="submit" class="submit-button">Send Message</button>
				</form>
			</div>

			<div class="contact-info">
				<div class="info-item">
					<h3>Order via WhatsApp</h3>
					<p>Chat with us directly to place an order or ask questions about our collection.</p>
					<a href="https://wa.me/62" target="_blank" rel="noopener noreferrer" class="cta-link">
						💬 Message on WhatsApp
					</a>
				</div>
				<div class="info-item">
					<h3>Follow Us</h3>
					<p>Stay updated with our latest collections and styling inspiration.</p>
					<a href="https://instagram.com/qashr.id" target="_blank" rel="noopener noreferrer" class="cta-link">
						📷 @qashr.id on Instagram
					</a>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.contact-section {
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

	.contact-content {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 60px;
	}

	.contact-form {
		background: hsl(35 56% 97%);
		padding: 40px;
		border-radius: 2px;
	}

	.form-group {
		display: flex;
		flex-direction: column;
		gap: 8px;
		margin-bottom: 24px;
	}

	.form-group label {
		color: hsl(20 30% 20%);
		font-weight: 500;
		font-size: 0.9rem;
	}

	.form-group input,
	.form-group textarea {
		padding: 12px 16px;
		border: 1px solid hsl(35 80% 70%);
		border-radius: 2px;
		font-family: inherit;
		font-size: 0.95rem;
		color: hsl(20 30% 20%);
		background-color: white;
		transition: border-color 0.3s ease;
	}

	.form-group input:focus,
	.form-group textarea:focus {
		outline: none;
		border-color: hsl(35 80% 50%);
		box-shadow: 0 0 0 3px rgba(204, 138, 51, 0.1);
	}

	.submit-button {
		width: 100%;
		padding: 14px 24px;
		background-color: hsl(20 30% 20%);
		color: hsl(35 56% 92%);
		border: none;
		border-radius: 2px;
		font-size: 0.9rem;
		font-weight: 500;
		cursor: pointer;
		transition: all 0.3s ease;
		text-transform: uppercase;
		letter-spacing: 0.5px;
	}

	.submit-button:hover {
		background-color: hsl(20 35% 30%);
		transform: translateY(-2px);
	}

	.contact-info {
		display: flex;
		flex-direction: column;
		gap: 40px;
	}

	.info-item {
		padding: 32px;
		background: linear-gradient(135deg, hsl(35 56% 97%) 0%, hsl(35 46% 98%) 100%);
		border-left: 3px solid hsl(35 80% 60%);
		border-radius: 2px;
	}

	.info-item h3 {
		font-size: 1.2rem;
		color: hsl(20 30% 20%);
		margin: 0 0 8px 0;
		font-family: ui-serif, Georgia, serif;
		font-weight: 400;
	}

	.info-item p {
		color: hsl(20 15% 35%);
		margin: 0 0 16px 0;
		font-size: 0.95rem;
		line-height: 1.6;
	}

	.cta-link {
		display: inline-block;
		color: hsl(20 30% 20%);
		text-decoration: none;
		font-weight: 500;
		border-bottom: 2px solid hsl(35 80% 60%);
		padding-bottom: 2px;
		transition: all 0.3s ease;
	}

	.cta-link:hover {
		color: hsl(35 80% 50%);
		border-bottom-color: hsl(20 30% 20%);
	}

	@media (max-width: 768px) {
		.contact-content {
			grid-template-columns: 1fr;
			gap: 40px;
		}

		.contact-form {
			padding: 32px 24px;
		}

		.section-title {
			font-size: 1.75rem;
		}

		.contact-section {
			padding: 60px 20px;
		}
	}
</style>
