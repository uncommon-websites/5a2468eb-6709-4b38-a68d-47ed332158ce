<script lang="ts">
	import { onMount, tick } from 'svelte';

	let mounted = false;
	let showModal = false;
	let fullName = '';
	let email = '';
	let submitted = false;
	let nameInput: HTMLInputElement | undefined;

	onMount(() => {
		mounted = true;
	});

	async function openModal() {
		showModal = true;
		await tick();
		nameInput?.focus();
	}

	function closeModal() {
		showModal = false;
	}

	function handleSubmit(e: Event) {
		e.preventDefault();
		// Handle form submission here
		console.log({ fullName, email });
		submitted = true;
		setTimeout(() => {
			showModal = false;
			submitted = false;
			fullName = '';
			email = '';
		}, 2000);
	}

	function handleKeydown(e: KeyboardEvent) {
		if (e.key === 'Escape') closeModal();
	}
</script>

<svelte:window on:keydown={handleKeydown} />


<section class="hero">
	<video class="hero-video" autoplay muted loop playsinline>
		<source src="/hero.webm" type="video/webm" />
		<source src="/hero.mp4" type="video/mp4" />
	</video>
	<div class="hero-overlay"></div>
	<div class="hero-gradient-left"></div>
	<div class="hero-gradient-right"></div>
	<div class="hero-line"></div>

	<div class="hero-content">
		<!-- Header -->
		<header class="header">
			<div class="logo" class:visible={mounted}>
				<img src="/logo-versa.svg" alt="Versa Villa by ARYA" class="logo-img" />
			</div>
			<p class="description" class:visible={mounted}>
				Born from resilience and engineered for peace of mind, our homes bring the protection you need together with the architecture that inspires — delivered in months, not years. Fire-resistant, pre-insured, and crafted with intention, each Versa Villa home is built to stand secure while feeling effortlessly refined.
			</p>
		</header>

		<!-- Main Content - Center Left -->
		<div class="main-content">
			<h1 class="headline">
				<span class="line" class:visible={mounted} style="--delay: 0.3s">
					<span class="line-inner">Versa Villa was created with one</span>
				</span>
				<span class="line" class:visible={mounted} style="--delay: 0.4s">
					<span class="line-inner">purpose: to rebuild stronger,</span>
				</span>
				<span class="line" class:visible={mounted} style="--delay: 0.5s">
					<span class="line-inner">safer, and more beautifully than</span>
				</span>
				<span class="line" class:visible={mounted} style="--delay: 0.6s">
					<span class="line-inner">ever before.</span>
				</span>
			</h1>
			<p class="description-mobile" class:visible={mounted}>
				Born from resilience and engineered for peace of mind, our homes bring the protection you need together with the architecture that inspires — delivered in months, not years. Fire-resistant, pre-insured, and crafted with intention, each Versa Villa home is built to stand secure while feeling effortlessly refined.
			</p>
			<button class="cta" class:visible={mounted} on:click={openModal}>
				<span class="cta-text">Sign up for updates</span>
				<span class="cta-arrow">→</span>
				<span class="cta-line"></span>
			</button>
		</div>
	</div>
</section>

<!-- Modal -->
{#if showModal}
	<!-- svelte-ignore a11y_click_events_have_key_events a11y_interactive_supports_focus -->
	<div class="modal-overlay" on:click={closeModal} role="dialog" aria-modal="true" tabindex="-1">
		<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_static_element_interactions -->
		<div class="modal" on:click|stopPropagation role="document">
			<button class="modal-close" on:click={closeModal} aria-label="Close">×</button>

			{#if !submitted}
				<h2 class="modal-title">Stay Updated</h2>
				<p class="modal-subtitle">Be the first to know about Versa Villa developments.</p>

				<form on:submit={handleSubmit} class="modal-form">
					<div class="form-field">
						<input
							type="text"
							bind:this={nameInput}
							bind:value={fullName}
							placeholder="Full Name"
							required
							class="form-input"
							autocomplete="off"
							data-1p-ignore
						/>
					</div>
					<div class="form-field">
						<input
							type="email"
							bind:value={email}
							placeholder="Email Address"
							required
							class="form-input"
							autocomplete="off"
							data-1p-ignore
						/>
					</div>
					<button type="submit" class="form-submit">
						<span>Subscribe</span>
						<span class="submit-arrow">→</span>
					</button>
				</form>
			{:else}
				<div class="success-message">
					<h2 class="modal-title">Thank you</h2>
					<p class="modal-subtitle">We'll be in touch soon.</p>
				</div>
			{/if}
		</div>
	</div>
{/if}

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}

	.hero {
		position: relative;
		width: 100%;
		height: 100vh;
		overflow: hidden;
	}

	.hero-video {
		position: absolute;
		top: 50%;
		left: 50%;
		min-width: 100%;
		min-height: 100%;
		width: auto;
		height: auto;
		transform: translate(-50%, -50%);
		object-fit: cover;
	}

	.hero-overlay {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(10, 12, 8, 0.7);
	}

	.hero-gradient-left {
		position: absolute;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 80%;
		background: radial-gradient(ellipse 80% 70% at 20% 80%, rgba(0, 0, 0, 0.45) 0%, transparent 100%);
		pointer-events: none;
		z-index: 1;
	}

	.hero-gradient-right {
		position: absolute;
		top: 0;
		right: 0;
		width: 100%;
		height: 60%;
		background: radial-gradient(ellipse 60% 80% at 85% 15%, rgba(0, 0, 0, 0.35) 0%, transparent 100%);
		pointer-events: none;
		z-index: 1;
	}

	.hero-line {
		position: absolute;
		top: 28%;
		left: 0;
		width: 100%;
		height: 1px;
		background: rgba(243, 243, 244, 0.15);
		z-index: 1;
	}

	.hero-content {
		position: relative;
		z-index: 1;
		height: 100%;
		width: 100%;
		color: #F3F3F4;
		display: flex;
		flex-direction: column;
	}

	/* Header */
	.header {
		padding: 2.5rem 5% 2.5rem 15%;
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		gap: 2rem;
	}

	.logo {
		opacity: 0;
		transform: translateY(-10px);
		transition: opacity 0.6s ease, transform 0.6s ease;
	}

	.logo.visible {
		opacity: 1;
		transform: translateY(0);
	}

	.logo-img {
		height: clamp(2.5rem, 4vw, 3.5rem);
		width: auto;
	}

	.description {
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(0.875rem, 1.25vw, 1.25rem);
		font-weight: 400;
		font-style: normal;
		line-height: normal;
		max-width: 32rem;
		margin: 0;
		text-align: justify;
		opacity: 0;
		transform: translateY(-10px);
		transition: opacity 0.6s ease 0.2s, transform 0.6s ease 0.2s;
		position: relative;
	}

	.description.visible {
		opacity: 1;
		transform: translateY(0);
	}

	/* Main Content */
	.main-content {
		flex: 1;
		display: flex;
		flex-direction: column;
		justify-content: center;
		padding: 0 15%;
		padding-bottom: 8rem;
		position: relative;
	}

	.headline {
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(1.75rem, 4vw, 3.5rem);
		font-weight: 400;
		font-style: normal;
		line-height: 1.1;
		margin: 0 0 3.5rem 0;
		letter-spacing: -0.02em;
		max-width: 45rem;
	}

	.line {
		display: block;
		overflow: hidden;
	}

	.line-inner {
		display: block;
		transform: translateY(100%);
		transition: transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
		transition-delay: var(--delay, 0s);
	}

	.line.visible .line-inner {
		transform: translateY(0);
	}

	/* CTA */
	.cta {
		display: inline-flex;
		align-items: center;
		gap: 0.5em;
		color: #F3F3F4;
		text-decoration: none;
		background: none;
		border: none;
		cursor: pointer;
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(1.5rem, 3vw, 2.75rem);
		font-weight: 400;
		position: relative;
		width: fit-content;
		letter-spacing: -0.02em;
		line-height: 1;
		opacity: 0;
		transform: translateY(20px);
	}

	.cta.visible {
		animation: ctaFadeIn 0.6s ease 0.9s forwards;
	}

	@keyframes ctaFadeIn {
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.cta.visible:hover {
		opacity: 1;
		transform: translateX(0.3em);
		transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), color 0.3s ease;
	}

	.cta::before {
		content: '';
		position: absolute;
		top: -0.15em;
		bottom: -0.15em;
		left: -0.3em;
		right: -0.3em;
		background: #F3F3F4;
		transform: scaleX(0);
		transform-origin: left;
		transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
		z-index: -1;
	}

	.cta:hover::before {
		transform: scaleX(1);
	}

	.cta:hover {
		color: black;
	}

	.cta-text {
		position: relative;
	}

	.cta-arrow {
		transition: transform 0.3s ease;
	}

	.cta:hover .cta-arrow {
		transform: translateX(0.1em);
	}

	.cta-line {
		position: absolute;
		bottom: -0.2em;
		left: 0;
		width: 100%;
		height: 1px;
		background: #F3F3F4;
		transition: background 0.3s ease;
	}

	.cta:hover .cta-line {
		background: black;
	}

	/* Responsive */
	@media (max-width: 1024px) {
		.header {
			padding: 2.5rem 8%;
		}

		.main-content {
			padding: 0 8%;
			padding-bottom: 6rem;
		}
	}

	@media (max-width: 768px) {
		.header {
			padding: 2rem 6%;
			flex-direction: column;
			gap: 1.5rem;
		}

		.description {
			max-width: 100%;
			text-align: left;
		}

		.main-content {
			padding: 0 6%;
			padding-bottom: 4rem;
		}
	}

	/* Mobile description - hidden by default, shown on mobile */
	.description-mobile {
		display: none;
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: 0.9375rem;
		font-weight: 400;
		line-height: 1.6;
		color: rgba(243, 243, 244, 0.85);
		margin: 1.5rem 0 2rem 0;
		max-width: 100%;
		opacity: 0;
		transform: translateY(10px);
		transition: opacity 0.6s ease 0.7s, transform 0.6s ease 0.7s;
	}

	.description-mobile.visible {
		opacity: 1;
		transform: translateY(0);
	}

	@media (max-width: 480px) {
		.description {
			display: none;
		}

		.description-mobile {
			display: block;
		}

		.main-content {
			padding-bottom: 3rem;
		}

		.headline {
			margin-bottom: 0;
			opacity: 0;
			transform: translateY(20px);
			transition: opacity 0.8s ease 0.3s, transform 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.3s;
		}

		.headline:has(.line.visible) {
			opacity: 1;
			transform: translateY(0);
		}

		/* Let text flow naturally on mobile */
		.line {
			display: inline;
		}

		.line-inner {
			display: inline;
			transform: none;
		}
	}

	/* Modal */
	.modal-overlay {
		position: fixed;
		inset: 0;
		background: rgba(10, 12, 8, 0.9);
		backdrop-filter: blur(8px);
		display: flex;
		align-items: center;
		justify-content: center;
		z-index: 100;
		animation: fadeIn 0.3s ease;
	}

	@keyframes fadeIn {
		from { opacity: 0; }
		to { opacity: 1; }
	}

	.modal {
		background: rgba(20, 24, 18, 0.95);
		border: 1px solid rgba(243, 243, 244, 0.1);
		padding: clamp(2rem, 5vw, 3.5rem);
		max-width: 28rem;
		width: 90%;
		position: relative;
		animation: slideUp 0.4s cubic-bezier(0.16, 1, 0.3, 1);
	}

	@keyframes slideUp {
		from {
			opacity: 0;
			transform: translateY(20px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.modal-close {
		position: absolute;
		top: 1rem;
		right: 1rem;
		background: none;
		border: none;
		color: #F3F3F4;
		font-size: 1.5rem;
		cursor: pointer;
		opacity: 0.5;
		transition: opacity 0.2s ease;
		line-height: 1;
		padding: 0.5rem;
	}

	.modal-close:hover {
		opacity: 1;
	}

	.modal-title {
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(1.5rem, 3vw, 2rem);
		font-weight: 400;
		color: #F3F3F4;
		margin: 0 0 0.75rem 0;
		letter-spacing: -0.02em;
	}

	.modal-subtitle {
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(0.875rem, 1.5vw, 1rem);
		color: rgba(243, 243, 244, 0.6);
		margin: 0 0 2rem 0;
		line-height: 1.5;
	}

	.modal-form {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.form-field {
		position: relative;
	}

	.form-input {
		width: 100%;
		background: transparent;
		border: none;
		border-bottom: 1px solid rgba(243, 243, 244, 0.2);
		padding: 0.75rem 0;
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(1rem, 1.5vw, 1.125rem);
		color: #F3F3F4;
		outline: none;
		transition: border-color 0.3s ease;
	}

	.form-input::placeholder {
		color: rgba(243, 243, 244, 0.4);
	}

	.form-input:focus {
		border-color: #F3F3F4;
	}

	.form-submit {
		display: inline-flex;
		align-items: center;
		gap: 0.5rem;
		background: #F3F3F4;
		color: #0a0c08;
		border: none;
		padding: 1rem 1.5rem;
		font-family: 'Neue Haas Grotesk Display', Helvetica, Arial, sans-serif;
		font-size: clamp(1rem, 1.5vw, 1.125rem);
		font-weight: 400;
		cursor: pointer;
		margin-top: 1rem;
		transition: background 0.3s ease, transform 0.3s ease;
		width: fit-content;
	}

	.form-submit:hover {
		background: #ffffff;
		transform: translateX(4px);
	}

	.submit-arrow {
		transition: transform 0.3s ease;
	}

	.form-submit:hover .submit-arrow {
		transform: translateX(4px);
	}

	.success-message {
		text-align: center;
		padding: 2rem 0;
	}
</style>
