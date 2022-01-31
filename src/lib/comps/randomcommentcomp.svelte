<script>
	export let content;
	export let contentSig;
	import { Card, CardBody, CardSubtitle, CardText } from 'sveltestrap';
</script>

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

<style>
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
