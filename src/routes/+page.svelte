<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Section from './Section.svelte';
	import { browser } from '$app/environment';
</script>

<svelte:head>
	<title>Educa US</title>
	<meta name="description" content="Educa US" />
</svelte:head>

<div class="full-width">
	<section>
		<video
			autoplay
			class="educa-video"
			muted
			src="https://rr3---sn-4g5ednsr.c.drive.google.com/videoplayback?expire=1679406674&ei=En4ZZNO_DK_r1bYPgLeNmAk&ip=169.150.197.246&cp=QVRMQUVfVVZVRVhPOkVpMHQ0VVpuMkstcHJpbHJybHJpa0tSWW82VHhWME9jX2ZPZC1mc2ZGejg&id=b4a6f58c46995c3c&itag=37&source=webdrive&requiressl=yes&mh=ci&mm=32&mn=sn-4g5ednsr&ms=su&mv=u&mvi=3&pl=26&ttl=transient&susc=dr&driveid=12mHw-6imiX1_bssn2nbYdliDEBa17LwP&app=explorer&mime=video/mp4&vprv=1&prv=1&dur=88.607&lmt=1679011278771191&mt=1679390996&subapp=DRIVE_WEB_FILE_VIEWER&txp=0011224&sparams=expire,ei,ip,cp,id,itag,source,requiressl,ttl,susc,driveid,app,mime,vprv,prv,dur,lmt&sig=AOq0QJ8wRgIhAMlZT5orn9CGCCAU7VxU3BXXPnOR8BRoXpsqieuhAQdQAiEAvA3xUP5bNYXw63w_HoIpj8yfkpHKPQUeVYBoQ1Oibs8=&lsparams=mh,mm,mn,ms,mv,mvi,pl&lsig=AG3C_xAwRQIgASFxiZOK9G3WSsX6WszWazagqmly3fswdQalV8MsgDICIQC-9i2aozhXDQYbecg1iWVn_fuKFj9e_OTjfvb9zqZlVg==&cpn=gK-7ToADIssCdkKm&c=WEB_EMBEDDED_PLAYER&cver=1.20230314.01.00"
		/>
	</section>
	<Section
		props={{ sectionId: 'test', title: 'IT', description: 'what??', color: '#ffffff', image: '' }}
	/>
	<!-- <Section
		props={{ sectionId: 'test', title: 'Health Care', description: 'what??', color: '', image: '' }}
	/> -->
</div>

<style>
	.full-width {
		width: 100%;
	}
	.educa-video {
		padding: 0 0 0 0;
		margin: 0 0;
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
