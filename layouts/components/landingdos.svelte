<script>
  let bgLandingImage = 'assets/images/alphacolor-unsplash.jpg';

  export let title;
</script>

<div>
  <div class="bgfx" style="background-image: url({bgLandingImage});">
  </div>
  <!-- colored slide -->

  <div class="bgfx nothalfy" style="background-image: url({bgLandingImage});">
    <div class="section-break-shade"></div>
    <div class="obah-rei-desu">
      <h1>[   {title}   ]</h1>
    </div>
  </div>
  <!-- shaded slide -->
</div><!-- section break fx -->


<style type="text/css">
  .bgfx {
    background: no-repeat bottom center fixed;
    background-size: cover;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100vh;
    overflow: hidden; /* clears white space above div! yey! */
  }

  .nothalfy {
    height: 100vh;
  }

  .section-break-shade {
    background-color: hsla(74, 75%, 30%, 0.66);
    width: 100%;
    height: 100vh;
  }

  .obah-rei-desu {
    width:  100%;
    height: 100%;
    margin-top: -100vh;
    color:  white;
  }

  h1 {
    margin:  0;
    text-align:  center;
    transform:  translateY(40vh);
    font-weight:  200;
    white-space:  pre;
  }

  /*.section-break-shade::after {
    content:  "yeah!";
    width: 50%;
    height:  50%;
    background-color: yellow;
  }*/

  .bg-pos {
    /*background-position: 0% 15%;*/
  }
</style>
