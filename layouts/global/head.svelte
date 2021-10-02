<script>
  export let title, env;
</script>

<head>
  <meta charset='utf-8'>
  <meta name='viewport' content='width=device-width,initial-scale=1'>

  <title>{ title }</title>

  <base href="{ env.local ? "/" : env.baseurl }">
  <script type="module" src="spa/ejected/main.js"></script>

  <link rel="preconnect" href="https://fonts.gstatic.com">
  <!-- <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@100;200;300;400;500;600;700&display=swap" rel="stylesheet"> -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@100;200;300;400;500;600;700&display=swap" rel="stylesheet">

  <link rel="icon" type="image/svg+xml" href="assets/logo.svg">
  <link rel='stylesheet' href='/assets/css/normalize.css'>
  <link rel='stylesheet' href='/assets/css/skeleton.css'>
  <link rel='stylesheet' href='/assets/css/extended.css'>
  <link href='https://api.mapbox.com/mapbox-gl-js/v2.3.1/mapbox-gl.css' rel='stylesheet' />

  <link rel='stylesheet' href='spa/bundle.css'>

  <script src='https://api.mapbox.com/mapbox-gl-js/v2.3.1/mapbox-gl.js'></script>
</head>
