<script>
	import { browser } from '$app/environment';
	import { onMount, onDestroy } from 'svelte';
	import education_section from '$lib/images/education_section.jpg';
	export let props = { sectionId: '', title: '', description: '', image: '', color: '' };
	const { sectionId, title, description, image, color = '#ffffff' } = props;
	let isActive = false;

	onMount(() => {
		const sections = document.querySelectorAll('.text-section');
		const difference = 150;
		const firstSection = sections[0];

		if (browser) {
			document.addEventListener('scroll', (e) => {
				// isActive = true;
				console.log(window.innerHeight);
				if (window.innerHeight - firstSection.getBoundingClientRect().top > 150) {
					firstSection.classList.add('active');
				}
			});
		}
	});
</script>

<div class="main-sections" style="background-image: url({image});">
	<div class="text-section">
		<h1>{title}</h1>
		<p>{description}</p>
		<pre>Learn more</pre>
	</div>
</div>

<style>
	:global(.text-section.active) {
		opacity: 1 !important;
		transform: translateX(0px) !important;
	}

	.main-sections {
		position: relative;
		background-repeat: no-repeat;
		background-size: auto !important;
		width: auto;
		height: 24rem;
		background-position: right top;
	}
	.text-section {
		width: 24rem;
		transform: translateX(-25px);
		display: flex;
		flex-direction: column;
		align-items: start;
		justify-content: start;
		padding: 1rem;
		opacity: 0;
		transition: all 1s ease-in-out;
		color: white;
		z-index: 3 !important;
	}
	.card {
		position: absolute;
		top: 0;
		background-color: white;
		height: 12rem;
		width: 24rem;
		padding: 1rem;
		opacity: 0.4;
		z-index: 0 !important;
		border-radius: 8%;
		margin: 8px;
	}
</style>
