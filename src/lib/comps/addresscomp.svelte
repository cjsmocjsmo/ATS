<script>
</script>

<div class="bar">
	<div class="addr1">
		<p>251 East Snow Cap Dr</p>
		<p>Belfair, WA 98528</p>
		<p>United States</p>
	</div>

	<div class="addr1">
		<p>License</p>
		<p>WA #604-037-042</p>
		<p>43 Falls PL</p>
		<p>Belfair, WA 98528</p>
	</div>

	<div class="addr1">
		<p>Bond</p>
		<p>#62922843</p>
		<p>Department Of Labor and Industries</p>
		<p>Contractor Registration</p>
		<p>PO Box 44450</p>
		<p>Olympia WA 98504-4450</p>
	</div>

	<div class="addr1">
		<p>Insurance</p>
		<p>#SII4851A201464</p>
		<p>Contractors Insurance NW</p>
		<p>PO Box 13033</p>
		<p>Olympia WA 98508</p>
	</div>
</div>

<style>
	.bar {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		align-items: center;
		margin-top: 1em;
	}

	@media (max-width: 500px) {
		.bar {
			flex-direction: column;
		}
	}

	.addr1 {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	p {
		font-weight: 700;
		font-size: 1em;
		color: white;
	}
</style>
