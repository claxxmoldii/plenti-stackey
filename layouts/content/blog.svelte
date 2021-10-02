<script>
  import Nav from "../global/nav.svelte";
  import Uses from "../components/source.svelte";

  // Svelte store example:
  import { count } from '../scripts/stores.svelte';
  import Incrementer from '../components/plenti/incrementer.svelte';
  import Decrementer from '../components/plenti/decrementer.svelte';
  let count_value;
  const unsubscribe = count.subscribe(value => {
    count_value = value;
  });

  // Content driven dynamic components example:
  export let components, allLayouts;
  export let title, body, author, date, store, content, shohei, arai;
</script>

<section class="" class:shohei class:arai>
  <div class="sticky">
    <Nav />
  </div>
  <div class="content container">
    <h1>{title}</h1>

    <p><em>{#if author}Written by {author}{/if}{#if date}&nbsp;on {date}{/if}</em></p>

    <div>
      {#each body as paragraph}
        <p>{@html paragraph}</p>
      {/each}
    </div>

    {#if store}
      <h3>The count is {count_value}</h3>
      <Incrementer/>
      <Decrementer/>
    {/if}

    {#if components}
      {#each components as { name }}
        <svelte:component this="{allLayouts["layouts_components_plenti_" + name + "_svelte"]}" />
      {/each}
    {/if}

    <Uses {content} />

    <p><a href="/">Back home</a></p>
  </div>
</section>

<style>
  section {
    min-height: calc(100vh - 40px);
  }

  .sticky {
    position: sticky;
    top: 0;
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
