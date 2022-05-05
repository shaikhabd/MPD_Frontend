<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans&family=Noto+Serif&display=swap" rel="stylesheet">
<script   src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous">
    import Hero from "../components/Hero.svelte";
    import Aboutcomp from "../components/Aboutcomp.svelte";
    import SearchArea from "../components/SearchArea.svelte";
    import Footer from "../components/Footer.svelte";
    import {fade , slide } from 'svelte/transition'
    import Navbar from "../components/Navbar.svelte";
</script>
<section transition:fade>
    <div class="bgholder">
    <Navbar />
    <Hero />
    </div>
    <Aboutcomp />
    <SearchArea />
    <Footer />
</section>

<style>
    .bgholder{
        background-size: contain;
        background-repeat: round;
        background-image: url("bg.jpeg"),linear-gradient(0deg, rgba(0,0,0,0.8104283949908089) 0%, rgba(255,255,255,0) 100%);
    }
    *{font-family: 'Noto Serif', serif;}

</style>