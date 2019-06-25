<script>
  // Routing
  import Router from "svelte-spa-router";
  import Home from "./pages/Home.svelte";
  import Select from "./pages/Select.svelte";
  import Switch from "./pages/Switch.svelte";
  import TabBar from "./pages/TabBar.svelte";
  import About from "./pages/About.svelte";
  import NotFound from "./pages/NotFound.svelte";

  // Navigation
  import AppDrawer from "./AppDrawer.svelte";

  // Routing
  const routes = {
    "/": Home,
    "/select": Select,
    "/switch": Switch,
    "/tabbar": TabBar,
    "/about": About,

    // Catch-all
    // This is optional, but if present it must be the last
    "*": NotFound
  };
</script>

<!-- Material Components Web CSS-->
<svelte:head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500">
  <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
  <link rel="stylesheet" href="https://unpkg.com/material-components-web@latest/dist/material-components-web.min.css">
</svelte:head>

<!-- Navigation-->
<AppDrawer title="Svelte Material Components" {routes}/>

<!-- Main app-->
<main>
  <br>
  <Router {routes}/>
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