<script>
	import { onMount } from 'svelte';
	let exception ; 
	onMount(() => {
		window.onunhandledrejection = (e) => {
		  exception = ('we got exception, but the app has crashed', e);
		}
	})
</script>

<nav
	style=" background-color: rgba(0, 0, 0,0.1); 
	width:100%"
	class="navbar"
	role="navigation"
	aria-label="main navigation"
>
	<div class="navbar-brand" id="navbar">
		<a href="/" class="navbar-item false">
			<label class="label" style="color: black; font-weight: 700 ; font-size: 20px;" for="title">Medicinal Plant Database</label>
		</a>
	</div>
	<div class="navbar-end">
		<div class="navbar-item">
			<div class="buttons Parentbutton">
				<a href="/" class="button bcolor false">
					<strong>Home</strong>
				</a>
				<a href="About" class="button bcolor false">
					<strong>About</strong>
				</a>
				<a href="#sb" class="button bcolor false">
					<strong>Search</strong>
				</a>
				<a href="src\routes\empty.svelte" class="button bcolor false">
					<strong>Tools</strong>
				</a>
				<a href="Help" class="button bcolor false">
					<strong>Help</strong>
				</a>
			</div>
		</div>
	</div>
</nav>

<style>
	.false {
		text-decoration: none;
	}
	.bcolor{
        background: none ;
		border: none;
		
	}
	.bcolor:hover{
		color: white;
	}

</style>


