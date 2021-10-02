<script>

</script>

<section class="landing fullBgImage">
  <h4>landing component... desu</h4>
  <p>full background image scrolls up and down</p>
  <p>writeable div independent of background image shade and opacity</p>
</section>

<style>
  .landing {
    width: 100%;
    height: 100vh;
    background-color: beige;

    background-image: linear-gradient(
    115deg,
    hsla(309, 100%, 10%, 0.7),
    hsla(309, 100%, 10%, 0.8)),
    url(../assets/images/huy-hung-trinh-toys-unsplash.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    color:  white;
  }

/*.fullBgImage::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100%;
  z-index: -1;
  background: crimson;
  background-image: linear-gradient(
    115deg,
    rgba(59, 122, 87, 0.8),
    rgba(59, 122, 87, 0.7)),
    url('../assets/hotStuff/jessierogers-01.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
}*/
</style>
