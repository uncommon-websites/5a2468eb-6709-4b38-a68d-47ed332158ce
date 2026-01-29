<script lang="ts">
	import "../app.css";
	import Header from "$lib/Header.svelte";
	import Footer from "$lib/Footer.svelte";
</script>

<div class="min-h-screen flex flex-col font-body bg-white text-gray-900 antialiased selection:bg-gray-200 selection:text-black">
	<Header />
	<main class="flex-grow w-full">
		<slot />
	</main>
	<Footer />
</div>
