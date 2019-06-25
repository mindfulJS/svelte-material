<script>
  // Drawer template
  import MDCDrawer from "/mdc/MDCDrawer.svelte";

  export let title;
  export let routes;
</script>

<!-- Drawer -->
<MDCDrawer {title} {routes} />