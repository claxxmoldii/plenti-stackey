<script>
  export let title, description;
</script>

<section>
  <div class="container">
    <h3>{title}</h3>
    <p>{description}</p>
    <p>whoah...</p>
  <ul>
    <li>created 'plenti-stackey' prototype plenti v.0.4.19
    <li>adjusted 'index.svelte' <span class="date">/2021.05.28</span></li>
    <li>added css <span class="date">/2021.05.28</span></li>
    <li>adjusted 'raleway' as main typeface <span class="date">/2021.05.28</span></li>
    <li>created 'buildlog' as --single type <span class="date">/2021.05.28</span></li>
    <br>

    <li>dropped 'tallfooter.svelte' from bodgie <span class="date">/2021.05.28</span></li>
    <li>dropped font-awesome from bodgie <span class="date">/2021.05.28</span></li>
    <li>tallfooter is okay <span class="date">/2021.05.28</span></li>
    <li>dropped footer copyright from bodgie <span class="date">/2021.05.28</span></li>
    <li>all content footer is turned into its own component. okay! <span class="date">/2021.05.28</span></li>
    <br>

    <li>dropped full-background iimage 'landing.svelte'. okay! <span class="date">/2021.05.28</span></li>
    <li>created 'reply' faux-component for testing. is okay. <span class="date">/2021.05.29</span></li>
    <li>updated to plenti v.0.4.20. yey! <span class="date rebuild">/2021.05.30</span></li>
    <li>updated to plenti v.0.4.21. yey! <span class="date rebuild">/2021.06.02</span></li>
    <li>rebuilt plenti-stackey still from plenti v.0.4.21. blog content 'store', now working! yey! <span class="date rebuild">/2021.06.08</span></li>
    <br>

    <li>a little components clean up... <span class="date">/2021.06.08</span></li>
    <li>created 'attributions' with plenti new type --single <span class="date">/2021.06.08</span></li>
    <li>rebuild: plenti v.0.4.24 <span class="date rebuild">/2021.06.19</span></li>
    <li>added mapboxgl <span class="date">/2021.06.27</span></li>
    <li>added static mapboxgl <span class="date">/2021.06.28</span></li>
    <br>

    <li>rebuild/updated: plenti v.0.4.25 <span class="date rebuild">/2021.07.20</span></li>
    <li>rebuilt okay! yosh! <span class="date">/2021.07.20</span></li>
    <li>rebuild/updated: plenti v.0.4.26 <span class="date rebuild">/2021.08.13</span></li>
    <li>rebuilt okay! tested! yosh! <span class="date">/2021.08.12</span></li>
    <li>updated tallfooter details... <span class="date">/2021.09.25</span></li>

    <li>updated tallfooter image... <span class="date">/2021.09.25</span></li>
    <li>updated maps! used kinuura ryo! yosh! yey mapbox! <span class="date">/2021.09.26</span></li>
    <li>'allcontent' fixed... added bgFX and minimal styling... <span class="date">/2021.09.29</span></li>
    <li>'landingdos' component fixed... <span class="date">/2021.09.30</span></li>

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

  .date.rebuild {
    color: hsla(360, 100%, 30%, 0.79);
    color:  hsla(196, 83%, 25%, 0.86);
    font-weight: 400;
  }
</style>
