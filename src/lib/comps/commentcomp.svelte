<script>
	let name = '';
	let message = '';
</script>

<div class="one">
	<form action="“”" method="“post”">
		<h3>Post A Review:</h3>
		<input type="“text”" name="“name”" value="Name (optional)" /> <br />
		<input type="“text”" name="“email”" value="Email" /> <br />
		<hr />
		<br /><textarea name="“message”" rows="“25”" cols="“120”" /><br />
		<input class="foo" type="submit" value="Post Review" />
	</form>
</div>

<style>
	h3 {
		color: whitesmoke;
	}

	form {
		min-width: 700px;
	}

	hr {
		color: white;
		height: 3px;
	}

	.one {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 700px;
	}

	.foo {
		font-size: 1.5em;
		max-height: 2.5em;
		width: 98.5%;
	}

	input {
		width: 50%;
		height: 3em;
		background-color: rgb(135, 205, 222);
		color: grey;
		border-radius: 7px;
		margin: 7px;
	}

	textarea {
		width: 100%;
		height: 15em;
		border-radius: 10px;
	}

	@media (max-width: 745px) {
		form {
			min-width: 250px;
		}
		textarea {
			min-width: 250px;
		}
		.foo {
			width: 250px;
		}
		.one {
			height: 575px;
		}
	}
</style>
