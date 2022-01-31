<script>
	import { Card, CardBody, CardSubtitle, CardText } from 'sveltestrap';
	const c1 = 'Curtis is very easy to work with and provides excellent services. ';
	const c2 = 'I look forward to hiring him again in the future.';
	const content = c1 + c2;
	const contentSig = '- Laura J';

	let visible = false;
	let setVisible = () => {
		if (visible) {
			visible = false;
		} else {
			visible = true;
		}
	};
</script>

<div>
	<p id="morerevs" on:click={setVisible}>more reviews >></p>
</div>

{#if visible}
	<div class="foo">
		<Card body color="info">
			<CardBody>
				<CardSubtitle>Reviews</CardSubtitle>
				<CardText>
					<p class="cbod">
						{content}
					</p>
					<p class="csig">
						{contentSig}
					</p>
				</CardText>
			</CardBody>
		</Card>
	</div>
{/if}

<style>
	p#morerevs {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: flex-end;
		margin: 0 2em 2em 0;
		color: white;
	}

	.cbod {
		font-style: italic;
	}

	.csig {
		float: right;
	}

	.foo {
		margin-top: 2em;
		max-width: 48%;
	}
    
	@media (max-width: 531px) {
		.foo {
			max-width: 100%;
			padding: 7px;
		}
	}
</style>
