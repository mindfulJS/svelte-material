<script>
  // Material Design Drawer component
  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  export let title;
  export let routes;
  // Get main routes as an array
  const routesArray = getRoutesArray(routes);

  onMount(() => {
    // Initialise Material Components Web
    mdc.autoInit();

    // Initialise drawer
    const drawer = mdc.drawer.MDCDrawer.attachTo(
      document.querySelector(".mdc-drawer")
    );
    const listEl = document.querySelector(".mdc-drawer .mdc-list");
    const mainContentEl = document.querySelector(".main-content");

    listEl.addEventListener("click", event => {
      drawer.open = false;
    });

    // Initialise topAppBar
    const topAppBar = mdc.topAppBar.MDCTopAppBar.attachTo(
      document.getElementById("app-bar")
    );
    topAppBar.setScrollTarget(document.getElementById("main-content"));

    topAppBar.listen("MDCTopAppBar:nav", () => {
      drawer.open = !drawer.open;
    });
  });

  function getRoutesArray(obj) {
    return Object.entries(obj).filter(e => {
      if (e[0] !== "*") {
        //console.log("key", e[0]);
        //console.log("value", e[1].name);
        return true;
      }
    });
  }
</script>

<!-- Drawer -->
<div class="drawer">
<header class="mdc-top-app-bar app-bar" id="app-bar">
    <div class="mdc-top-app-bar__row">
      <section class="mdc-top-app-bar__section mdc-top-app-bar__section--align-start">
        <a href="#" class="material-icons mdc-top-app-bar__navigation-icon">menu</a>
        <span class="mdc-top-app-bar__title">{title}</span>
      </section>
    </div>
  </header>
  <aside class="mdc-drawer mdc-drawer--modal" data-mdc-auto-init="MDCDrawer">
    <div class="mdc-drawer__content">
      <nav class="mdc-list">
        {#each routesArray as route, i}
          {#if i === 0}
            <a class="mdc-list-item mdc-list-item--activated" href="#{route[0]}" aria-current="page">
              <span class="mdc-list-item__text">{route[1].name}</span>
            </a>
          {:else}
            <a class="mdc-list-item" href="#{route[0]}">
              <span class="mdc-list-item__text">{route[1].name}</span>
            </a>
          {/if}
        {/each}
      </nav>
    </div>
  </aside>

  <div class="mdc-drawer-scrim"></div>
  <div id="main-content" class="main-content">
  </div>
</div>

<style>
  .drawer {
    display: flex;
    height: 10vh;
  }

  .main-content {
    overflow: auto;
    height: 100%;
  }

  .app-bar {
    position: absolute;
  }
</style>