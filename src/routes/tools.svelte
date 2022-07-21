<script>
import Navbar from "../components/Navbar.svelte";
</script>

<Navbar />
<section style="padding: 3%;">
<h1 style="font-weight: 600; font-size: xx-large; color: #4caae7;">Available Tools</h1><br>
<!-- <div style="display:flex; justify-content:space-evenly">
<button style="display:flex;align-items:center; justify-content:center; font-weight: 600;color:black;width: 50vw;height: 10vh; font-size:larger ;background-color:#22b36c;border: none;"><a href="https://share.streamlit.io/shaikhabd/tools/main/tool2.py">Fragments generation of smiles</a></button>
</div> -->
<div style="display:flex; justify-content:space-evenly">
  <button style="display:flex;align-items:center; justify-content:center; font-weight: 600;color:black;width: 50vw;height: 10vh; font-size:larger ;background-color:#22b36c;border: none;"><a href="https://mitmpd-moledits.netlify.app" target=”_blank”>Molecular Editor</a></button>
  </div>
<div style="display:flex; justify-content:space-evenly">
<button style="display:flex;align-items:center; justify-content:center; font-weight: 600;color:black;width: 50vw;height: 10vh; font-size:larger ;background-color:#22b36c;border: none;"><a href="https://molsoft.com/mprop/mprop.cgi" target=”_blank”>Drug-Likeness and molecular property prediction</a></button>
</div>
<div style="display:flex; justify-content:space-evenly">
  <button style="display:flex;align-items:center; justify-content:center; font-weight: 600;color:black;width: 50vw;height: 10vh; font-size:larger ;background-color:#22b36c;border: none;"><a href="https://molview.org/" target=”_blank”>Molecular View</a></button>
  </div>
  <div style="display:flex; justify-content:space-evenly">
    <button style="display:flex;align-items:center; justify-content:center; font-weight: 600;color:black;width: 50vw;height: 10vh; font-size:larger ;background-color:#22b36c;border: none;"><a href="http://chemmine.ucr.edu/eisearch/query/" target=”_blank”>Structural Similarity Search</a></button>
    </div>
</section>


<!-- <section class="cards">
<div class="card">
  <h3>Title one</h3>
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum accusamus harum dolor maxime vitae voluptatum veniam magnam saepe. Voluptatem, dolore atque fugiat eligendi officiis nemo quae beatae possimus nisi explicabo?</p>
  <button>View Tool</button>
</div>

</section> -->


<style>

  .card{
    width: 15vw;
    height: 35vh;
  }
    a{
    font-size: large;
  }
    a:link {
    color:white;
   text-decoration: none;
    }
    a:visited {
  color: white;
  background-color: transparent;
  text-decoration: none;
}
    a:active {
  color: white;
  background-color: transparent;
  text-decoration: none;
}
a:hover {
  color:aliceblue;
  background-color: transparent;
  text-decoration: none;
}
button:hover{
    background-color: white;
}
  div{
     position: relative;
     margin: 1%;
  }
</style>


