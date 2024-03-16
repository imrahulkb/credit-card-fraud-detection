<script>
	// export let name;
	// import '../app.css';
	import Navbar from './Navbar.svelte';
	import Home from './Home.svelte';
	import Dash from './Dash.svelte';
	// import Dashboard from './routes/Dashboard.svelte';
	// import Dashboard from './Dashboard.svelte';
	import '@fontsource/montserrat'
	import '@fontsource/mulish'
	// import { Router } from 'svelte-spa-router';


	// const routes={
	// 	'/Dashboard/*':Dashboard,
	// }
	
</script>


<main>
	<!-- <Router {routes}/> -->
	

	<Navbar/>
	<Home />
	<Dash/>
	<!-- <Dashboard/> -->
	</main>

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