<script>
  export let title, intro, components, content, allContent, map;
  import Grid from '../components/grid.svelte';
  import Uses from "../components/source.svelte";
  import Pager from "../components/pager.svelte";

  import LandingDos from '../components/landingdos.svelte';
  import Nav from '../global/nav.svelte';
  import AllContent from "../components/allcontent.svelte";
  import TallFooter from "../components/tallfooter.svelte";

  import KinuuraRyo from "../components/kinuuraRyo.svelte";
  import KinuuraRyoStatic from "../components/kinuuraRyoStaticMap.svelte";

  import Issues from "../components/issuestofix.svelte";

  $: currentPage = content.pager;
  let postsPerPage = 3;
  let allPosts = allContent.filter(content => content.type == "blog");
  let totalPosts = allPosts.length;
  let totalPages = Math.ceil(totalPosts / postsPerPage);
  $: postRangeHigh = currentPage * postsPerPage;
  $: postRangeLow = postRangeHigh - postsPerPage;
</script>

<div class="notorumaitidesu">
  <LandingDos {title} />
  <nav class="sticky">
    <Nav />
  </nav>

  <section id="intro" class="intro">
    <div class="container">
      <h1>{title}</h1>
      {#each intro as paragraph}
        <p>{@html paragraph}</p>
      {/each}
    </div>
  </section>

  <!-- <section>
    <div class="container">
      <div>
        <h3>Recent blog posts:</h3>
        <Grid items={allPosts} {postRangeLow} {postRangeHigh} />
        <br />
      </div>
      <Pager {currentPage} {totalPages} />
      <Uses {content} />
    </div>
  </section> -->

  <KinuuraRyo />
  <!-- <KinuuraRyoStatic /> -->

  <AllContent {allContent}/>
  <Issues />
</div>

<TallFooter {title}/>
  <!-- tallfooter is on different stacking conttext -->


<style>
  section {
    min-height: 100vh;
  }

  .sticky {
    position:  sticky;
    top:  0;
    /*background-color: hsla(173, 18%, 82%, 1);*/
    z-index: 100;
  }

  .intro {
    background-color: beige;
    padding-top:  100px;
  }

  .blog {
    background-color: aliceblue;
    padding: 0 100px;
    padding-top: 40px;
  }

  .allcontent {
    background-color: darkseagreen;
  }

  .allcontent > * {
    margin-top: 50%;
    /*transform:  translateY(-50%);*/
  }

  .orumaitidesu {
    /*z-index:  200;*/
  }
</style>
