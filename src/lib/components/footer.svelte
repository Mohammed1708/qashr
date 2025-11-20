<footer class="footer">
	<div class="container">
		<div class="footer-content">
			<div class="footer-brand">
				<h3>Qashr.id</h3>
				<p>Elegance of the Kingdom</p>
				<p class="tagline">Saudi-inspired craftsmanship for the modern noble</p>
			</div>
			
			<div class="footer-links">
				<div class="link-group">
					<h4>Collection</h4>
					<ul>
						<li><a href="#products">Sulthoni Series</a></li>
						<li><a href="#about">About</a></li>
						<li><a href="#contact">Contact</a></li>
					</ul>
				</div>
				<div class="link-group">
					<h4>Connect</h4>
					<ul>
						<li><a href="https://instagram.com/qashr.id" target="_blank">Instagram</a></li>
						<li><a href="https://wa.me/62" target="_blank">WhatsApp</a></li>
					</ul>
				</div>
			</div>
		</div>

		<div class="footer-bottom">
			<p>&copy; 2025 Qashr.id. All rights reserved.</p>
			<p>Elegance of the Kingdom — Inspired by Saudi nobility, crafted for modern modesty.</p>
		</div>
	</div>
</footer>

<style>
	.footer {
		background-color: hsl(20 30% 20%);
		color: hsl(35 56% 92%);
		padding: 60px 20px 40px;
	}

	.container {
		max-width: 1200px;
		margin: 0 auto;
	}

	.footer-content {
		display: grid;
		grid-template-columns: 2fr 1fr;
		gap: 60px;
		margin-bottom: 60px;
		border-bottom: 1px solid hsl(35 80% 40%);
		padding-bottom: 40px;
	}

	.footer-brand h3 {
		font-size: 1.5rem;
		font-family: ui-serif, Georgia, serif;
		font-weight: 400;
		margin: 0 0 8px 0;
		letter-spacing: -0.5px;
	}

	.footer-brand > p {
		margin: 0 0 4px 0;
		color: hsl(35 80% 60%);
		font-size: 0.9rem;
	}

	.tagline {
		color: hsl(20 15% 70%) !important;
		font-size: 0.85rem;
		margin-top: 12px;
	}

	.footer-links {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 40px;
	}

	.link-group h4 {
		font-size: 0.9rem;
		text-transform: uppercase;
		letter-spacing: 1px;
		margin: 0 0 16px 0;
		color: hsl(35 80% 60%);
		font-weight: 500;
	}

	.link-group ul {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.link-group li {
		margin-bottom: 12px;
	}

	.link-group a {
		color: hsl(35 56% 92%);
		text-decoration: none;
		font-size: 0.9rem;
		transition: color 0.3s ease;
	}

	.link-group a:hover {
		color: hsl(35 80% 60%);
	}

	.footer-bottom {
		text-align: center;
	}

	.footer-bottom p {
		margin: 0 0 8px 0;
		font-size: 0.85rem;
		color: hsl(20 15% 70%);
	}

	.footer-bottom p:last-child {
		margin-bottom: 0;
		color: hsl(35 80% 60%);
	}

	@media (max-width: 768px) {
		.footer-content {
			grid-template-columns: 1fr;
			gap: 40px;
		}

		.footer-links {
			grid-template-columns: 1fr;
		}

		.footer {
			padding: 40px 20px 30px;
		}
	}
</style>
