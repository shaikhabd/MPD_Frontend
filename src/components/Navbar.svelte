<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css">
<script>
	import { onMount } from 'svelte';

	onMount(() => {
		const targetDiv = document.getElementsByClassName('rs-align');
		const btn = document.getElementsByClassName('menu-toggle');

		btn.onclick = function () {
			if (targetDiv.style.display == 'none') {
				targetDiv.style.display = 'flex';
			} else {
				targetDiv.style.display = 'none';
			}
		};
	});
</script>

<nav class="navbar nav-style" role="navigation" aria-label="main navigation">
	<div class="set full navbar-brand" id="navbar">
		<a href="/" class="navbar-item false ">
			<!-- <label class="rs-phone" for="title">Powered by</label> -->
		</a>
		<img src="https://www.mitbio.edu.in/wp-content/themes/mitsbrs/assets/images/logo.png" alt="https://www.mitbio.edu.in/wp-content/themes/mitsbrs/assets/images/logo.png"/>
	</div>
    
	<button class="menu-toggle">
		<span class="bar" />
		<span class="bar" />
		<span class="bar" />
	</button>
	<div class="navbar-end">
		<div class="navbar-item">
			<div class="rs-align buttons Parentbutton">
				<a href="/" class="button bcolor false">
					<strong>Home</strong>
				</a>
				<a href="https://mitmpd.netlify.app/About" class="button bcolor false">
					<strong>About</strong>
				</a>
				<a href="https://mitmpd.netlify.app/#sb" class="button bcolor false">
					<strong>Search</strong>
				</a>
				<a href="https://mitmpd.netlify.app/tools" class="button bcolor false">
					<strong>Tools</strong>
				</a>
				<a href="https://mitmpd.netlify.app/Help" class="button bcolor false">
					<strong>Help</strong>
				</a>
			</div>
		</div>
	</div>
</nav>

<style>
	.nav-style {
		background-color:white;
		height: 15vh;
		padding-left: 5%;
		padding-right: 5%;
	}
	.set {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}
	img {
		position: relative;
		top: -10%;
		left: 0%;
		width: 85%;
		height: 80%;
	}
	.rs-align {
		display: flex;
	}

	.menu-toggle {
		top: 0.7rem;
		right: 2%;
		position: absolute;
		display: none;
		flex-direction: column;
		justify-content: space-between;
		height: 30px;
		width: 40px;
		background: none;
		padding: 0%;
		margin: 0%;
		border: none;
	}
	.bar {
		width: 100%;
		border-radius: 10%;
		border: 2px solid rgb(36, 36, 36);
	}
	.false {
		text-decoration: none;
	}
	.bcolor {
		background: none;
		border: none;
	}
	.bcolor:hover {
		color: rgb(16, 176, 16);
	}
	.rs-phone {
		color: black;
		font-weight: 700;
		font-size: 8px;
	}

	@media screen and (max-width: 1050px) {
		.set {
			display: flex;
			flex-direction: column;
			align-items: flex-start;
			height: 100%;
		}
		.rs-phone {
			font-size: 8px;
		}
		.menu-toggle {
			display: flex;
		}
		.rs-align {
			display: none;
		}
		img {
			height: 100px;
			width: 200px;
		}
	
	}
	@media screen and (max-width:1100px){
		.nav-style{
			padding-left: 0%;
			padding-right: 0%;
		}
	}
</style>














