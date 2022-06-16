<script context="module">
	export async function load({ fetch , params }) {
		const res = await fetch('http://localhost:8080/Search/compound/'+params.id);
		const data = await res.json();
		if (res.ok) {
			return {
				props: { DataBySpeciesName: data }
			};
		}
	}
</script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css">
<script src="https://3Dmol.org/build/3Dmol-min.js">
import Footer from "../../components/Footer.svelte";
import Navbar from "../../components/Navbar.svelte";
export let DataBySpeciesName;
</script>

<section style="width:100%;">
	<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"
integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p"
crossorigin="anonymous"> </script>
	<Navbar />
	<div class="gcolor" style="padding: 0.6%;">
		<h1 style="font-weight: 700; font-size: larger; margin-left: 20vw; color: white;">
			Compound Summary 
		</h1>
	</div>
	<section style="display: flex;">
	<div style="width: 20%; background-color: aliceblue;top: 1%;">
		<ul style="position: sticky; top: 1%; padding: 7%;list-style-type: disc; color: black;">
			<li style="margin: 5%;"><a class ="linker"href="#ci">Compound Information</a></li>
			<li  style="margin: 5%;"><a  class ="linker"href="#tg">Target Gene</a> </li>
			<li  style="margin: 5%;"><a  class ="linker"href="#tp">Target Protein</a> </li>
		</ul>
	</div>
    {#if DataBySpeciesName == ""}
	<p>Compound Not Found</p>
{:else}
<div style="margin-left: 1%; margin-right: 1%; padding-bottom: 2%; width:100%;">
 <br>
<div id="ci" class="bg-holder curve" style=" background-color: aliceblue;">
<h1 class="curve gcolor" style=" background:linear-gradient(180deg, #4bf7aa 0%, #63f636 100%); padding: 1.3%; font-size: larger; color:white; margin-bottom: 2%;font-weight: 600;">Compound Information</h1>
<p class="space" ><label for="text">Name: </label>{DataBySpeciesName[0].Name_of_small_molecule_or_Compound}</p><hr>
<p class="space" ><label for="text">PubChem_Id: </label><a target="_blank" href="{DataBySpeciesName[0].PubChem_link}">{DataBySpeciesName[0].PubChem_Id}</a></p><hr>
<p class="space"><label for="text">DrugBank_Id: </label><a target="_blank" href="{DataBySpeciesName[0].Drugbank_link}">{DataBySpeciesName[0].Drugbank_inactive}</a></p><hr>
<p class="space"><label for="text">Structure:</label></p>
<img style="margin-left: 2%;" height="100" width="200" src="https://go.drugbank.com/structures/{DataBySpeciesName[0].Drugbank_inactive}/image.svg" alt="image not available">
<p style="margin-left: 2%; font-weight: 300;">Smiles: {DataBySpeciesName[0].SMILES}</p>
<!-- {DataBySpeciesName[0].drugBank_Id} -->
<button class="sbutton"><a target="_blank" style="text-decoration: none; color: white;" href="http://localhost:8080/mol3Dview/{DataBySpeciesName[0].Name_of_small_molecule_or_Compound}">View 3D Structure</a></button>
<hr>
<p class="space"><label for="text">Mode Of Action: </label>{DataBySpeciesName[0].MoA}</p><hr>
<p class="space"><label for="text">Side_Effects_or_Toxicity: </label>{DataBySpeciesName[0].Side_Effects_or_Toxicity}</p><hr>
</div>
<br>

<div class="curve" id="tg" style="background-color: aliceblue;">
<h1 class="curve gcolor" style="padding: 1.3%; font-size: larger; color: white;margin-bottom: 2%; font-weight: 600;">
	Target Gene
</h1>
<table class="table table-striped" style="width: 100%; background-color: aliceblue;">
	<thead>
		<tr>
		
		  <th scope="col">Gene Name</th>
		  <th scope="col">NCBI id</th>
		</tr>
	  </thead>
	  {#each DataBySpeciesName as count}
	  <tbody>
		<tr>
		  <td>{count.Gene_Name}</td>
		  <td><a target="_blank" href="{count.Gene_link}">{count.Target_gene_NCBI_Link}</a></td>
		</tr>
		{/each}
  </table>
  <hr>
</div>


<div class="curve" id="tp" style="background-color: aliceblue;">
    <h1 class="curve gcolor" style="padding: 1.3%; font-size: larger; color: white;margin-bottom: 2%; font-weight: 600;">
        Target Protein
    </h1>
	 
	<table border="0" class="table table-striped" style="width: 100%; background-color: aliceblue;">
		<thead>
			<tr>
			  <th scope="col">Protein Name</th>
			  <th scope="col">Uniprot id</th>
			</tr>
		  </thead>
		  {#each DataBySpeciesName as count}
		  <tbody>
			<tr>
			  <td>{count.Protein_Name}</td>
			  <td><a target="_blank" style="text-decoration: none;" href="{count.Protein_link}">{count.Target_Protein_Uniprot_Link}</a></td>
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
	.sbutton{
		margin-top:1%;
		margin-left: 2%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 6px 14px;
  font-family: -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
  border-radius: 6px;
  border: none;

  color: #fff;
  background: linear-gradient(180deg, #4bf7a7 0%, #63f636 100%);
   background-origin: border-box;
  box-shadow: 0px 0.5px 1.5px rgba(54, 122, 246, 0.25), inset 0px 0.8px 0px -0.25px rgba(255, 255, 255, 0.2);
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.sbutton:focus {
  box-shadow: inset 0px 0.8px 0px -0.25px rgba(255, 255, 255, 0.2), 0px 0.5px 1.5px rgba(54, 122, 246, 0.25), 0px 0px 0px 3.5px rgba(58, 108, 217, 0.5);
  outline: 0;
}
.linker{
		color: black;
		font-weight: 600;
	}
	.linker:hover{
		border-bottom: solid black 1.5px;
	}
	.gcolor{
		background:linear-gradient(180deg, #4bf7a7 0%, #63f636 100%);
	}
	.curve{
		border-top-left-radius: 15px;
		border-top-right-radius: 15px;	
	}
	*{font-family: 'Noto Serif', serif;}
	.sbutton:hover{
		background: linear-gradient(180deg, #1ff792 0%, #42fe09 100%);
	}
</style>
<Footer />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans&family=Noto+Serif&display=swap" rel="stylesheet">