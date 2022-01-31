<script>
	import svlogo from '$lib/images/svelte.png';
	import cfsvg from '$lib/images/cloudflare/cf-logo-h-white.svg';
	import fbsvg from '$lib/images/firebase/fb-white.svg';
</script>

<div class="fdiv">
	<img class="sveltesvg" src={svlogo} alt="fuckit" />
	<img class="cloudflaresvg" src={cfsvg} alt="fuckit" />
	<img class="firebasesvg" src={fbsvg} alt="fuckit" />
</div>

<style>
	.fdiv {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}

	.sveltesvg {
		width: 35px;
	}
	.cloudflaresvg {
		width: 175px;
	}

	.firebasesvg {
		width: 300px;
	}

	@media (max-width: 500px) {
		.fdiv {
			flex-direction: column;
		}
	}
</style>
