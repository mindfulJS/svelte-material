<script>
  // Material Deisgn Button component
  // buttonText: needed for button text
  // onClickFunction: needed to call function on click

  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  export let buttonText;
  export let onClickFunction;

  onMount(() => {
    // Initialise Material Components Web
    mdc.autoInit();
  });
</script>

<!-- Button -->
<div>
  <button class="mdc-button mdc-button--raised" on:click={onClickFunction} data-mdc-auto-init="MDCRipple">
    <span class="mdc-button__label">{buttonText}</span>
  </button>
</div>