<script>
	let firstName = 'Jon';
	let lastName = 'Christie';
	let color = '#d35400'

	$: name = firstName + ' ' + lastName

	const toggle = ()=> {
		color = color == 'blue' ? 'red' : 'blue'
	}
</script>

<!-- OUTPUT / HTML  -->
<main>
	<h1 style="color: {color}">Hello {name}!</h1>

	<!-- <button on:click={()=> color = 'purple'}>CLICK ME </button> -->
	<button on:click={toggle}>CLICK ME </button>
</main>

<!-- STYLE TAGS  -->
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