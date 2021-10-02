<script>
  export let title, description, author, content, shohei, arai, isit, isBlog, allContent;

  import Nav from "../global/nav.svelte";
  import Uses from "../components/source.svelte";

  import Grid from '../components/grid.svelte';
  import AllContent from "../components/allcontent.svelte";
  import Pager from "../components/pager.svelte";

  $: currentPage = content.pager;
  let allPosts = allContent.filter(content => content.type == "blog");
  let totalPosts = allPosts.length;
  let totalPages = Math.ceil(totalPosts / postsPerPage);
  $: postRangeHigh = currentPage * postsPerPage;
  $: postRangeLow = postRangeHigh - postsPerPage;
</script>

<section class="" class:shohei class:arai>
  <div class="sticky">
    <Nav />
  </div>
  <div class="content container">
    <h1>{title}</h1>

    <div>
      {#each description as paragraph}
        <p>{@html paragraph}</p>
      {/each}
    </div>

    {#if !isit}
      <Uses {content} />
      <p><a href=".">Back home</a></p>
    {/if}

    {#if isit}
      <p>{author}</p>
    {/if}

    {#if isBlog}
      <hr>
      <section>
        <div class="container">
          <div>
            <h3>Recent blog posts:</h3>
            <Grid items={allPosts} {postRangeLow} {postRangeHigh} />
            <br />
          </div>
          <Pager {currentPage} {totalPages} />
          <Uses {content} />
        </div>
      </section>
    {/if}
  </div>
</section>

<style>
  section {
    min-height: calc(100vh - 40px);
  }

  .sticky {
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .isFlex {
    flex-direction:  column;
  }

  .content {
    padding-top:  100px;
  }

  .shohei {
    background-color: hsla(273, 19%, 90%, .9);
  }

  .arai {
    background-color: hsla(57, 29%, 90%, .9);
  }
</style>
