<script>
  // Material Design Drawer component

  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

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

    document.body.addEventListener("MDCDrawer:closed", () => {
      mainContentEl.querySelector("input, button").focus();
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
</script>

<!-- Drawer -->



<div class="drawer">
<header class="mdc-top-app-bar app-bar" id="app-bar">
    <div class="mdc-top-app-bar__row">
      <section class="mdc-top-app-bar__section mdc-top-app-bar__section--align-start">
        <a href="#" class="material-icons mdc-top-app-bar__navigation-icon">menu</a>
        <span class="mdc-top-app-bar__title">Svelte Material Components</span>
      </section>
    </div>
  </header>
  <aside class="mdc-drawer mdc-drawer--modal" data-mdc-auto-init="MDCDrawer">
    <div class="mdc-drawer__content">
      <nav class="mdc-list">
        <a class="mdc-list-item mdc-list-item--activated" href="#" aria-current="page">
          <i class="material-icons mdc-list-item__graphic" aria-hidden="true">inbox</i>
          <span class="mdc-list-item__text">Inbox</span>
        </a>
        <a class="mdc-list-item" href="#">
          <i class="material-icons mdc-list-item__graphic" aria-hidden="true">send</i>
          <span class="mdc-list-item__text">Outgoing</span>
        </a>
        <a class="mdc-list-item" href="#">
          <i class="material-icons mdc-list-item__graphic" aria-hidden="true">drafts</i>
          <span class="mdc-list-item__text">Drafts</span>
        </a>
      </nav>
    </div>
  </aside>

  <div class="mdc-drawer-scrim"></div>
  <div id="main-content" class="main-content">
    <div id="nav1">Hello</div>
  </div>
</div>

<style>
  .drawer {
    display: flex;
    height: 10vh;
  }

  .mdc-drawer-app-content {
    flex: auto;
    overflow: auto;
    position: relative;
  }

  .main-content {
    overflow: auto;
    height: 100%;
  }

  .app-bar {
    position: absolute;
  }
</style>