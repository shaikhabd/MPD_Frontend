<script context="module">
	export async function load({ fetch , params }) {
		const res = await fetch('http://backendexpress-env.eba-mstkmt6p.us-east-1.elasticbeanstalk.com/Search/therapeuticEffect/'+params.id);
		const data = await res.json();
		if (res.ok) {
			return {
				props: { DataBySpeciesName: data }
			};
		}
	}
</script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"
integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p"
crossorigin="anonymous">
import Footer from "../../components/Footer.svelte";
import Navbar from "../../components/Navbar.svelte";

export let DataBySpeciesName;
</script>

<section style="width:100%;">
	<Navbar />
	
	<div class="gcolor" style="padding: 0.6%;">
		<h1 style="font-weight: 700; font-size: larger; margin-left: 20vw; color: white;">
			Result for {DataBySpeciesName[0].Therapeutic}
		</h1>
	</div>
	<section style="display: flex;">
	<div style="width: 20%; background-color: aliceblue;top: 1%;">
		<ul style="position: sticky; top: 1%; padding: 7%;list-style-type: disc; color: black;">
			<li  style="margin: 5%;"><a  class ="linker"href="#gi">Therapeutic Category</a> </li>
		</ul>
	</div>
    {#if DataBySpeciesName == ""}
	<p>Search Not Found</p>
{:else}
<div style="margin-left: 1%; margin-right: 1%; padding-bottom: 2%; width:100%;">
<br>
<div id="cl" class="curve" style="background-color: aliceblue;">
<h1 class="curve gcolor" style=" padding: 1.3%; font-size: larger; color: white;margin-bottom: 2%; font-weight: 600;">
	Therapeutic Category 
</h1>

<table border="0" class="table table-striped" style="width: 100%; background-color: aliceblue;">
	<thead>
		<tr>
		  <th scope="col">Compound</th>
		  <th scope="col">Plant Name</th>
		</tr>
	  </thead>
	  {#each DataBySpeciesName as count}
	  <tbody>
		<tr>
		  <td>{count.Name_of_small_molecule_or_Compound}</td>
		  <td>{count.Common_Name}</td>
		</tr>
		{/each}
  </table>
<hr>
</div>

</div>
{/if}
</section>
</section>
<!-- <button style="position: fixed; bottom: 10vh; left: 90vw; border:2px solid; border-radius: 100%; height: 10vh; width: 10vh; background-color:teal; border-color: teal;"><a href="#navbar" style="text-decoration: none; color: aliceblue;">Back to Top</a></button> -->
<style>
    label{
        font-weight: 700;
    }
	#navbar{
		position: relative;
	}
    hr{
    background:rgba(156, 148, 152, 0.3);
	height: 0.1vh;
    }
    .space{
        margin-left: 2%;
    }
	.linker{
		color: black;
		font-weight: 600;
	}
	.linker:hover{
		border-bottom: solid black 1.5px;
	}
	.gcolor{
		background:linear-gradient(180deg, #4caae7 0%, #64b6ec 100%);
		
	}
	.curve{
		border-top-left-radius: 15px;
		border-top-right-radius: 15px;	
	}
	*{font-family: 'Noto Serif', serif;}
</style>
<Footer />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans&family=Noto+Serif&display=swap" rel="stylesheet">