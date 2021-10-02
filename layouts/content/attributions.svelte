<script>
  export let title, tagline;
</script>

<section>
  <div class="container">
    <h3>{title}</h3>
    <p>{tagline}</p>
    <p>whoah...</p>
    <ul>
      <li>plenti</li>
      <li>svelte</li>
      <li>skeleton css</li>
      <li>google fonts/raleway</li>
      <li>manis/yurizal susanto</li>
      <li>font awesome</li>
    </ul>
</div>
</section>

<style>
  section {
    min-height:  100vh;
  }

  ul {
    grid-area: list;
    padding-bottom: 100px;
  }

  li {
    color: rgba(0,0,0,0.7);
    font-size: 1.6rem;
    list-style: none;
  }

  .date {
    color: lightskyblue;
    padding-left:  10px;
  }
</style>
