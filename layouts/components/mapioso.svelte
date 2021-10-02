<script>
  import { onMount } from 'svelte';

  onMount(() => {
      mapboxgl.accessToken =
        'pk.eyJ1IjoiY2xheHhtb2xkaWkiLCJhIjoiY2txY2FpdXY2MDI0MjJwcGg4cmJmczQ3aCJ9.ETsOxzEKnOggZspWV_jHZg';
      var map = new mapboxgl.Map({
      container: 'map', // container ID
      style: 'mapbox://styles/mapbox/streets-v11', // style URL
      center: [121.1052, 14.6155], // starting position [lng, lat], greenpark, cainta
      // center: [34.8671937, 136.9758875], // starting position [lng, lat], dai-3 kinuura-ryo
      zoom: 16 // starting zoom
    });
  });
</script>

<section>
  <div id='map' style='width: 100%; height: 100%;'></div>
</section>

<style>
  section {
    height: 100vh;
    background-color: pink;
  }
</style>

<!-- each map gets unique access token -->
