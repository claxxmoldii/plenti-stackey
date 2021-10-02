<script>
  import { makeTitle } from '../scripts/make_title.svelte';
  export let allContent;
</script>

<section class="bgFX">
  <div class="isBorder">
    <span>All content:</span>
    {#each allContent as content}
      <a href="{content.path}">{makeTitle(content.filename)}</a>
    {/each}
  </div>
</section>

<style>
  section {
    height: 100vh;
    display: flex;
    align-items: center;
    background-color: var(--base-dark);
    margin-top: 100px;
    flex-shrink: 0;

    font-weight:  200;
  }

  section > * {
    margin: 0 auto;
  }

  span {
    color: var(--primary);
    font-weight: 300;
  }

  a {
    color: white;
    text-decoration: none;
    margin-left: 10px;
  }

  a:hover {
    color: lightskyblue;
  }

  .isBorder {
    border:  #333 solid 1px;
    padding:  10px;
    padding-left: 20px;
    padding-right: 20px;
    border-radius: 20px;
    background-color: black;
  }

  .bgFX {
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
    background-position: top;

    color:  white;
  }
</style>
