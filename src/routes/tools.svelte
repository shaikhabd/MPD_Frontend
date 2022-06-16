<script>
import Navbar from "../components/Navbar.svelte";
</script>

<Navbar />
<section style="padding: 3%;">
<h1 style="font-weight: 600; font-size: xx-large; color: #4caae7;">Available Tools</h1><br>
<div style="display:flex; justify-content:space-evenly">
<button style="display:flex;align-items:center; justify-content:center; font-weight: 600;color:black;width: 50vw;height: 10vh; font-size:larger ;background-color:#22b36c;border: none;"><a href="https://share.streamlit.io/shaikhabd/tools/main/tool2.py">Fragments generation of smiles</a></button>
</div>
</section>

<style>
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
</style>


