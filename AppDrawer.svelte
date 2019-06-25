<script>
  // Drawer template
  import MDCDrawer from "./mdc-templates/MDCDrawerTemplate.svelte";

  export let title;
  export let routes;
</script>

<!-- Drawer -->
<MDCDrawer {title} {routes} />