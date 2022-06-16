<section id="home" class="size" style="background-color: #0072bc	;">
  <div class="parent spacing"  >
    <img src="dna.svg" alt="">
    <div child>
    <p class="rs-phone">
      Welcome to MIT MPD<span class=""></span> 
    </p>
    <p style="font-weight: 400; font-size: large; text-align: center;">
      A paradigm shift from herbal medicines to modern drug discovery.</p>
  </div>
</div>
<script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12">
</script>
<script>
var typed  = new Typed(".auto-input" ,{
strings:["MIT" ,"Medicinal","Plant" ,"Database"],
typeSpeed:100 ,
backSpeed:100,
loop: true 
}); 
</script>

</section>

<style>
  .size{
    position: relative;
    height: 60vh;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 4;
  }
.spacing{
  display: inline;
  position: relative;
  z-index: 3;
}
img{
  position: absolute;
  height: 50vh;
  width: 40vh;
  right: -30%;
  z-index: -1;
  fill: aliceblue;
}
.rs-phone{
  font-size: 70px; 
  text-align: center;
}
@media screen and (max-width:600px){
.rs-phone{
  text-align: center;
  font-size: xx-large;
}
.size{
  height: 40vh;
}
}
</style>


