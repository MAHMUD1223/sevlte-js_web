<script>
	//export let name;

	let namu = "Mom";
	let pow = 33;
	const increase = () => {
		pow++;
	};

    let color = "blue";
	const inputer = (e) => {
		color = e.target.value;
	};
	const clicker = (e) => {
		color = "red"
	};
</script>

<main>
	<div>
		<h1>Hello {namu}!</h1>
	 	<p>Thank you mom Your power is {pow}</p>
		<button on:click={increase} >Increase</button>
	</div>
	
	<div>
		<h1>Taking input</h1>
		<p style="color: {color};">See what is your favorite color ?<br> {color} </p>
		<button on:click={clicker}>Change</button>
		<!-- <input type="text" on:input={inputer} value="{color}"> -->
		<input type="text" bind:value={color}>
	</div>
</main>


<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>