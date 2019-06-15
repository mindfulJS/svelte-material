<!-- Instantiate single textfield component rendered in the document -->
<script>
  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  onMount(() => {
    mdc.autoInit();
  });
</script>

<div class="mdc-select" data-mdc-auto-init="MDCSelect">
  <i class="mdc-select__dropdown-icon"></i>
  <select class="mdc-select__native-control">
    <option value="" disabled selected></option>
    <option value="grains">
      Bread, Cereal, Rice, and Pasta
    </option>
    <option value="vegetables">
      Vegetables
    </option>
    <option value="fruit">
      Fruit
    </option>
  </select>
  <label class="mdc-floating-label">Pick a Food Group</label>
  <div class="mdc-line-ripple"></div>
</div>

