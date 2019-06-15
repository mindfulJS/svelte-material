<script>
  // Main app
  import AppTitle from "./AppTitle.svelte";
  import AppJson from "./AppJson.svelte";
</script>

<!-- Material Components Web CSS-->
<svelte:head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500">
  <link rel="stylesheet" href="https://unpkg.com/material-components-web@latest/dist/material-components-web.min.css">
</svelte:head>

<!-- Main app-->
<main>
  <AppTitle />
  <AppJson />
</main>

<style>
  main {
    text-align: center;
    width: 80%;
    margin: auto;
  }
</style>