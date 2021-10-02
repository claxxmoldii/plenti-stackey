<script>
  import { onMount } from 'svelte';

  onMount(() => {
    mapboxgl.accessToken =
        'pk.eyJ1IjoiY2xheHhtb2xkaWkiLCJhIjoiY2txY2FpdXY2MDI0MjJwcGg4cmJmczQ3aCJ9.ETsOxzEKnOggZspWV_jHZg';

    var map = new mapboxgl.Map({
      container: 'map',
      style: 'mapbox://styles/mapbox/streets-v11',
      center: [136.9753, 34.8673],
      zoom: 16,
      scrollWheelZoom: false
    });

    map.scrollWheelZoom.disable();
  });
</script>

<section class="isGrid">
  <div id='map' class="isDaMap" style='width: 100%; height: 100%;'></div>
  <div class="isDaMapDescription">
    <p>that is kinuura ryo on the left... yeah!</p>
  </div>
</section>

<style>
  section {
    height: 100vh;
    background-color: pink;
  }

  .isGrid {
    grid-template-columns: 1fr 1fr;
  }
</style>

<!-- each map gets unique access token -->
<!-- map is kinuura ryo -->
