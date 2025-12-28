<script lang="ts">
	import "../app.css";
</script>

<div class="min-h-screen flex flex-col font-body bg-white text-gray-900 antialiased selection:bg-gray-200 selection:text-black">
	<main class="flex-grow w-full">
		<slot />
	</main>
</div>
