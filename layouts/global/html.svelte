<script>
  import Head from './head.svelte';
  import Nav from './nav.svelte';
  // import Footer from './footer.svelte';
  import { makeTitle } from '../scripts/make_title.svelte';

  export let content, layout, allContent, allLayouts, env;
</script>

<html lang="en">
<Head title={makeTitle(content.filename)} {env} />

<body class="isFlex">
  <!-- <Nav /> -->
  <main>
    <svelte:component
      this= {layout}
            {...content.fields}
            {content}
            {allContent}
            {allLayouts}
    />
  </main>
  <!-- <Footer {allContent} /> -->
  <footer>
    <!-- <div>copyright &copy; 2021, {content.fields.title}</div> -->
    <div>&copy; fuaitoo! 2021</div>
  </footer>
  <script src="https://kit.fontawesome.com/80f1b342a4.js" crossorigin="anonymous"></script>
</body>
</html>

<style>
  html, body {
    height: 100%;
  }

  body {
    font-family: 'Raleway', sans-serif;
    display: flex;
    flex-direction: column;
    margin: 0;
  }

  .isFlex {
    flex-direction:  column;
  }

  footer {
    font-family: 'Raleway', sans-serif;
    text-align:  center;
    font-size: 1.5rem;
    font-weight: 100;
    color:  white;
    background-color: hsl(205, 79%, 66%);
    padding: 8px;
    justify-self: flex-end;
  }

  :global(:root) {
    --primary: rgb(34, 166, 237);
    --primary-dark: rgb(16, 92, 133);
    --accent: rgb(254, 211, 48);
    --base: rgb(245, 245, 245);
    --base-dark: rgb(17, 17, 17);
  }

  /*main {
    flex: 1 0 auto;
  }
  :global(.container) {
    max-width: 1024px;
    margin: 0 auto;
    flex-grow: 1;
    padding: 0 20px;
  }
  :global(:root) {
    --primary: rgb(34, 166, 237);
    --primary-dark: rgb(16, 92, 133);
    --accent: rgb(254, 211, 48);
    --base: rgb(245, 245, 245);
    --base-dark: rgb(17, 17, 17);
  }
  :global(main a) {
    position: relative;
    text-decoration: none;
    color: var(--base-dark);
    padding-bottom: 5px;
  }
  :global(main a:before) {
    content: "";
    width: 100%;
    height: 100%;
    background-image: linear-gradient(to top, var(--accent) 25%, rgba(0, 0, 0, 0) 40%);
    position: absolute;
    left: 0;
    bottom: 2px;
    z-index: -1;
    will-change: width;
    transform: rotate(-2deg);
    transform-origin: left bottom;
    transition: width .1s ease-out;
  }
  :global(main a:hover:before) {
    width: 0;
    transition-duration: .15s;
  }*/
</style>
