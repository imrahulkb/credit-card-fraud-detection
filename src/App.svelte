<script>
	import Navbar from './Navbar.svelte';
	import Home from './Home.svelte';
	import Dash from './Dash.svelte';
	import '@fontsource/montserrat'
	import '@fontsource/mulish'
	import { Router,Route } from 'svelte-routing';
</script>

<Router>
	<Navbar /> 
	<Route path="/" component={Home} />
	<Route path="/dash" component={Dash} />
  </Router>

<style>
	main {
		text-align: center;
		/* padding: 1em; */
		max-width: 240px;
		margin: 0 auto;
		/* background-color: black; */
		/* background-size: cover; */
	}

	

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>