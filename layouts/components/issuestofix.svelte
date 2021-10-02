<script>
  // export let title, description;
</script>

<section>
  <div class="container">
    <h3>issues to fix...</h3>

    <ul>
      <li>
        <div class="issues">
          <h4>page needs reloading when...</h4>
          <p>clicking on pagination pages/first/last/prev/next...</p>
          <p>clicking on blogposts...</p>
          <p>clicking on nav links 'stackey', 'about' & 'contact us'... </p>
        </div>
      </li>
      <li>
        <div class="issues">
        </div>
      </li>
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

  h3 {
    color:  pink;
    padding-top: 15vh;
  }

  .issues p {
    padding-left: 50px;
  }

  .date {
    color: lightskyblue;
    padding-left:  10px;
  }

  .date.rebuild {
    color: hsla(360, 100%, 30%, 0.79);
    color:  hsla(196, 83%, 25%, 0.86);
    font-weight: 400;
  }
</style>
