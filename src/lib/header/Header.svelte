<script>
	export const prerender = true;
	import { Image } from 'sveltestrap';
	import p1 from '$lib/images/same1.webp';
	import p2 from '$lib/images/same2.webp';
	import p3 from '$lib/images/same3.webp';
	import p4 from '$lib/images/same4.webp';
	import p5 from '$lib/images/same5.webp';
	import p6 from '$lib/images/same6.webp';
	import p7 from '$lib/images/same7.webp';
	import p8 from '$lib/images/same8.webp';

	let alist = [p1, p2, p3, p4, p5, p6, p7, p8];
	let url = p1;

	function shuffleArray(alist) {
		for (let i = alist.length - 1; i > 0; i--) {
			const j = Math.floor(Math.random() * (i + 1));
			[alist[i], alist[j]] = [alist[j], alist[i]];
		}
		console.log(alist);
	}

	let i = 0;
	let idx = 0;
	let intr = setInterval(function () {
		url = alist[idx];
		if (i++ == 5500) clearInterval(intr);
		if (idx++ == 7) {
			shuffleArray(alist);
			idx = 0;
		}
	}, 6000);

</script>

<header>
	<div class="banner">
		<Image fluid alt="fuckti" src={url} />
	</div>
</header>

<style>
	.banner {
		display: flex;
		flex-direction: column;
		max-height: 500px;
		min-height: 109px;
	}
</style>
