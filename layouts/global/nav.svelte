<nav>
  <div class="container">
    <span id="brand"><a href="."><img alt="planarian" src="assets/logo.svg" />Home</a></span>
    <a href="stackey">stackey</a>
    <a href="blog">blog</a>
    <a href="about">about</a>
    <a href="contact">contact</a>
  </div>
</nav>

<style>
  nav, .container, #brand, #brand a {
    display: flex;
    background-color: hsla(173, 18%, 82%, 1);
  }
  nav {
    min-height: 60px;
    /*box-shadow: 0px 2px 3px var(--base);*/
  }
  #brand {
    flex: 1;
  }
  a {
    align-self: center;
    align-items: center;
    color: var(--base-dark);
    text-decoration: none;
    padding-left:  20px;
  }
  img {
    margin-right: 10px;
  }
</style>
