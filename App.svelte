<script>
  // Main app
  import AppDrawer from "./AppDrawer.svelte";
  import AppTitle from "./AppTitle.svelte";
  import AppCards from "./AppCards.svelte";
</script>

<!-- Material Components Web CSS-->
<svelte:head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500">
  <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
  <link rel="stylesheet" href="https://unpkg.com/material-components-web@latest/dist/material-components-web.min.css">
</svelte:head>

<AppDrawer />
<!-- Main app-->
<main>
  
  <AppTitle />
  <AppCards />
  
</main>

<style>
  :global(body) {
    /* this will apply to <body> */
    margin: 0;
  }

  main {
    text-align: center;
    width: 80%;
    margin: auto;
  }
</style>