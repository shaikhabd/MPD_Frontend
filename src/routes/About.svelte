<script>
import Navbar from "../components/Navbar.svelte";
import Footer from "../components/Footer.svelte";
</script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css" />
<link
	href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
	rel="stylesheet"
	integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3"
	crossorigin="anonymous"
/>

<section style="position: relative;">
	<Navbar />
</section>

<section style="background-color: aqua;">
</section>
<section class="hero is-halfheight">
	<div class="maindiv">
		<p style="color: #82E0AA;" class="title">About the Database</p>
		<p>
			Medicinal plant database is an online, comprehensive,free to access online database containing information about various medicinal plants. It is a bioinformatics resource which is used to study the biodiversity of indigenous medicinal plants found across the world by extracting the active phytochemicals from the data collected and to analyse their efficacy against multidrug drug resistant pathogens. 

 It is a one stop solution to analyze the molecular interaction between identified virulent bacterial targets and natural products.
		</p>
		<br />
		<h2 style="color: #82E0AA;">List of Plants Available</h2>
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
	.maindiv {
		padding: 2%;
	}
</style>
