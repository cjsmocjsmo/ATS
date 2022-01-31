<script context="module">
	// // Import the functions you need from the SDKs you need
	// import { initializeApp } from 'firebase/app';
	// // TODO: Add SDKs for Firebase products that you want to use
	// // https://firebase.google.com/docs/web/setup#available-libraries

	// // Your web app's Firebase configuration
	// const firebaseConfig = {
	// 	apiKey: 'AIzaSyAca22jv3pCzTPVTDH21UU-f-tAlMseaX0',
	// 	authDomain: 'atsreviews-5afab.firebaseapp.com',
	// 	projectId: 'atsreviews-5afab',
	// 	storageBucket: 'atsreviews-5afab.appspot.com',
	// 	messagingSenderId: '624798621609',
	// 	appId: '1:624798621609:web:e0aa9db26ff0c5b892aeb8'
	// };

	// // Initialize Firebase
	// const app = initializeApp(firebaseConfig);

	export const prerender = true;
	import Commentcomp from '$lib/comps/commentcomp.svelte';
	import Randomcommentcomp from '$lib/comps/randomcommentcomp.svelte';
	import MoreRevs from '$lib/comps/morereviewscomp.svelte';
	import { Icon, Button, Card, CardBody, CardHeader, CardTitle } from 'sveltestrap';
	import pic1 from '$lib/images/pic1.webp';
	import pic2 from '$lib/images/pic2.webp';
	import pic3 from '$lib/images/pic3.webp';
	import { is_client } from 'svelte/internal';
	import FAB from '$lib/comps/floatingActionButton.svelte';

	let content = 'I contacted Curtis about removing several, dangerous trees on my property.';
	content += '  He showed up on time and ready to work. He did exactly what I expected him';
	content += ' to do. He does exceptional work. I will continue to call Curtis when I need';
	content += ' a tree removed. I would highly recommend Alphatree.';
	const contentSig = ' - Dan do1058';

	let content2 = 'Curtis and crew took down an 80’ fir near a fence and house. NO DAMAGE!!!';
	content2 += '  Cleanup was thorough and they cut the rounds into 14” rounds for later';
	content2 += ' splitting. Crew had a great attitude. Will use them again.';
	const constent2Sig = ' - Kurt R';

	let content3 = 'Here at Alpha Tree Service we specialize in removing trees of all kinds ';
	content3 += 'from some of the tightest spaces and homes here in Washington.  With 15 years of ';
	content3 += 'experience in the tree industry Alpha Tree Service has the tools and experience ';
	content3 += 'needed to get the job done safely and on time.  When bad weather blows through ';
	content3 += 'and trees fall, no matter  if it has fallen on your home or in your yard, ';
	content3 += 'we are here to help clean up the mess.  We will do our best to leave your ';
	content3 += 'property as we found it.';
</script>

<svelte:head>
	<title>Alpha Tree Service</title>
</svelte:head>

<a href="tel:360 516 8933"><p id="tnum">360 516 8933</p></a>
<p id="tnum2">Alpha Tree Service</p>

<div class="counties">
	<div class="foo">
		<Card class="mb-3">
			<CardHeader>
				<CardTitle>Mason County</CardTitle>
			</CardHeader>
			<CardBody>
				<img class="cardimg" src={pic1} alt="fuckit" />
			</CardBody>
		</Card>
	</div>
	<div class="foo">
		<Card class="mb-3">
			<CardHeader>
				<CardTitle>Kitsap County</CardTitle>
			</CardHeader>
			<CardBody>
				<img class="cardimg" src={pic2} alt="fuckit" />
			</CardBody>
		</Card>
	</div>
	<div class="foo">
		<Card class="mb-3">
			<CardHeader>
				<CardTitle>Pierce County</CardTitle>
			</CardHeader>
			<CardBody>
				<img class="cardimg" src={pic3} alt="fuckit" />
			</CardBody>
		</Card>
	</div>
</div>

<div class="box2">
	<div id="IFrame" style="margin: .25em">
		<iframe 
			width="490" 
			height="280" 
			src="https://www.youtube.com/embed/PHDLlOBqkjw" 
			title="YouTube video player" 
			frameborder="0" 
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
			allowfullscreen>
		</iframe>
	</div>
	<div id="IFrame" style="margin: .25em">
		<iframe
			width="490"
			height="280"
			src="https://www.youtube.com/embed/okVkEfmoTTA"
			title="YouTube video player"
			frameborder="0"
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
			allowfullscreen
		/>
	</div>
</div>

<hr />
<p class="introTxt">{content3}</p>
<p class="introSig"> - Curtis McBride</p>
<hr />

<!-- <div class="box2">
	<div id="IFrame">
		<iframe 
			width="490" 
			height="280" 
			src="https://www.youtube.com/embed/PHDLlOBqkjw" 
			title="YouTube video player" 
			frameborder="0" 
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
			allowfullscreen>
		</iframe>
	</div>
	<div id="IFrame">
		<iframe
			width="490"
			height="280"
			src="https://www.youtube.com/embed/okVkEfmoTTA"
			title="YouTube video player"
			frameborder="0"
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
			allowfullscreen
		/>
	</div>
</div> -->

<div class="box2">
	<div id="IFrame2" style="margin: .25em">
		<iframe 
			width="490" 
			height="280" 
			src="https://www.youtube.com/embed/CVi0d1aepbE" 
			title="YouTube video player" 
			frameborder="0" 
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
			allowfullscreen>
		</iframe>
	</div>
	<div id="IFrame2" style="margin: .25em">
		<iframe
			width="490"
			height="280"
			src="https://www.youtube.com/embed/MAhLq6x6jOM"
			title="YouTube video player"
			frameborder="0"
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
			allowfullscreen
		/>
	</div>
</div>


<div class="reviewback">
	<div class="box1">
		<Randomcommentcomp {content} {contentSig} />
		<Randomcommentcomp content={content2} {contentSig} />
	</div>

	<MoreRevs />

	<Commentcomp />
</div>

<FAB />

<style>

	.introTxt {
		font-style: italic;
		font-size: 1.25em;

	}

	.introSig {
		display: flex;
		flex-direction: row;
		justify-content: end;
		align-items: center;
	}

	.reviewback {
		background-color: rgb(75, 95, 211);
		border-radius: 15px;
		margin-top: 2em;
		margin-bottom: 2em;
	}

	p#tnum {
		font-size: 3em;
		text-align: center;
		font-weight: 900;
	}

	p#tnum2 {
		font-size: 1.75em;
		text-align: center;
		font-weight: 700;
	}

	.counties {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
	}

	.foo {
		max-width: 230px;
	}

	.cardimg {
		max-width: 190px;
		margin: auto;
	}

	@media (max-width: 500px) {
		.cardimg {
			width: 87px;
		}
	}
	/* .fbi {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		margin-top: 10px;
		margin-bottom: 20px;
	} */

	a {
		text-decoration: none;
	}

	.box1 {
		display: flex;
		flex-direction: row;
		align-items: top;
		justify-content: space-around;
	}

	.box2 {
		display: flex;
		flex-direction: row;
		align-items: center;
		margin-top: 2em;
	}

	@media (max-width: 769px) {
		.box2 {
			flex-direction: column;
		}
	}

	@media (max-width: 531px) {
		iframe {
			width: 370px;
			height: 187px;
		}
		
		.box1 {
			flex-direction: column;
		}
	}

	@media (max-width: 365px) {
		iframe {
			width: 310px;
			height: 175px;
		}
	}
</style>
