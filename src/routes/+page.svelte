<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Section from './Section.svelte';
	import educa_video from '$lib/videos/educa_video.mp4';
	import { browser } from '$app/environment';
	import education_section from '$lib/images/education_section.jpg';
</script>

<svelte:head>
	<title>Educa US</title>
	<meta name="description" content="Educa US" />
</svelte:head>

<div class="full-width">
	<section>
		<video autoplay loop class="educa-video" muted src={educa_video} />
	</section>
	<Section
		props={{
			sectionId: 'test',
			title: 'IT',
			description:
				'Occaecat dolor ut eiusmod nostrud esse dolore amet mollit amet sit voluptate tempor. Eiusmod reprehenderit nulla tempor consequat culpa reprehenderit exercitation exercitation quis laborum id magna sunt aliquip. Elit esse cillum consectetur exercitation minim minim minim quis.',
			color: '#ffffff',
			image: education_section
		}}
	/>
	<Section
		props={{ sectionId: 'test', title: 'Health Care', description: 'what??', color: '', image: '' }}
	/>
</div>

<style>
	.full-width {
		width: 100%;
	}
	.educa-video {
		padding: 0 0 0 0;
		margin: 0 0;
		width: 100%;
	}
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
