
<script>
import Navbar from "../components/Navbar.svelte";
import Footer from "../components/Footer.svelte";
</script>

<section style="position: relative;">
	<Navbar />
</section>

<section style="background-color: aqua; ">
</section>
<section class="hero is-halfheight">
	<div class="maindiv">
		<p style="color: #22b36c;" class="title">About the Database</p>
		<p>
			Medicinal plant database is an online, comprehensive,free to access online database containing information about various medicinal plants. It is a bioinformatics resource which is used to study the biodiversity of indigenous medicinal plants found across the world by extracting the active phytochemicals from the data collected and to analyse their efficacy against multidrug drug resistant pathogens. 

 It is a one stop solution to analyze the molecular interaction between identified virulent bacterial targets and natural products.
		</p>
		<br />
		<h2 style="color: #22b36c;font-size: large; font-weight: 620;">List of Plants Available</h2>
		<ul>
			<li>• Alder - Alnus</li>
			<li>• Black alder – Alnus glutinosa, Ilex verticillata</li>
			<li>• Common alder – Alnus glutinosa</li>
			<li>• False alder – Ilex verticillata</li>
			<li>• Gray alder – Alnus incana</li>
			<li>• Speckled alder – Alnus incana</li>
			<li>• White alder – Alnus incana, Alnus rhombifolia, Ilex verticillata</li>
			<li>• Almond – Prunus dulcis</li>
			<li>• Aloe vera – Aloe vera</li>
			<li>• Amaranth – Amaranthus</li>
			<li>• Foxtail amaranth – Amaranthus caudatus</li>
			<li>• Ambrosia</li>
			<li>• Tall ambrosia – Ambrosia trifida</li>
			<li>• Amy root – Apocynum cannabinum</li>
			<li>• Angel trumpet – Brugmansia suaveolens</li>
		</ul>
	</div>
</section>
<section>
	<Footer />
</section>

<style>
	img{
    position: absolute;
	z-index: -1;
	height: 50vh;
	width: 50vw;
	bottom: 0%;
	right: 0%;
	}
	.maindiv {
		padding: 2%;
	}
</style>
