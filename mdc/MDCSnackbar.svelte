<script>
  // Material Design Snackbar component
  //
  // It needs to be opened by parent component from the onMount function
  // This is useful for asynchronised functions like loading data.
  // Add the following to the parent component:
  //
  //   onMount(() => {
  //     document.querySelector(".mdc-snackbar").MDCSnackbar.open();
  //   });

  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  export let message;

  onMount(() => {
    mdc.autoInit();
  });
</script>

<div class="mdc-snackbar" data-mdc-auto-init="MDCSnackbar">
  <div class="mdc-snackbar__surface">
    <div class="mdc-snackbar__label"
         role="status"
         aria-live="polite">
      {message}
    </div>
  </div>
</div>