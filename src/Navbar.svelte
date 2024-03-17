<script>
  import '@fontsource/montserrat'
  import '@fontsource/mulish'
  import {Link} from 'svelte-routing'
  </script>

<nav class="navbar"> 
	<img src="/images/logo.png" alt="logo" class="logo">
	<div class="nav-links">
		<Link class='a' to="/">Home</Link>
		<Link class='a' to="/dash">Dashboad</Link>
	</div>
</nav>
<style>
	.navbar{
		display: flex;
		align-items: centre;
		background-color: black;
		/* height: 50px; */
		color: white;
		padding: 25px 15px;
	}
	.logo{
	
		width: 150px;
		height:50px;
		margin-right: 70px;
		margin-left: 40px;

	}
	.nav-links {
		height:50px;
        align-items: center;
        display: flex;
    }

	.nav-links a{
		color:white;
		text-decoration: none;
		margin-right: 50px;
		align-items: center;
	    font-size: 20px;
		/* text-transform: uppercase; */
	}

</style>


