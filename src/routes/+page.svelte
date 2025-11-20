<script lang="ts">
	import Hero from '$lib/components/hero.svelte';
	import About from '$lib/components/about.svelte';
	import Products from '$lib/components/products.svelte';
	import Advantages from '$lib/components/advantages.svelte';
	import Testimonials from '$lib/components/testimonials.svelte';
	import Contact from '$lib/components/contact.svelte';
	import Footer from '$lib/components/footer.svelte';
	import ProductDetailsModal from '$lib/components/product-details-modal.svelte';

	let selectedProduct: any = $state(null);
	let isModalOpen = $state(false);

	function handleViewDetails(product: any) {
		selectedProduct = product;
		isModalOpen = true;
	}

	function handleCloseModal() {
		isModalOpen = false;
		selectedProduct = null;
	}
</script>

<main>
	<Hero />
	<About />
	<Products viewDetails={handleViewDetails} />
	<Advantages />
	<Testimonials />
	<Contact />
	<Footer />
	
	<ProductDetailsModal 
		product={selectedProduct} 
		isOpen={isModalOpen} 
		onClose={handleCloseModal}
	/>
</main>

<style>
	main {
		width: 100%;
	}
</style>
