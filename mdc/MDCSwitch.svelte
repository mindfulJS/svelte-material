<script>
  // Material Design Switch component

  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  onMount(() => {
    // Initialise Material Components Web
    mdc.autoInit();
  });
</script>

<!-- Switch -->
<div class="mdc-switch" data-mdc-auto-init="MDCSwitch">
  <div class="mdc-switch__track"></div>
  <div class="mdc-switch__thumb-underlay">
    <div class="mdc-switch__thumb">
        <input type="checkbox" id="basic-switch" class="mdc-switch__native-control" role="switch">
    </div>
  </div>
</div>
<label for="basic-switch">off/on</label>