<!-- Instantiate single textfield component rendered in the document -->
<script>
  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  onMount(() => {
    mdc.autoInit();
  });
</script>
<!--
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
-->
<div class="mdc-select" data-mdc-auto-init="MDCSelect">
  <input type="hidden" name="enhanced-select">
  <i class="mdc-select__dropdown-icon"></i>
  <div class="mdc-select__selected-text"></div>
  <div class="mdc-select__menu mdc-menu mdc-menu-surface demo-width-class">
    <ul class="mdc-list">
      <li class="mdc-list-item mdc-list-item--selected" data-value="" aria-selected="true"></li>
      <li class="mdc-list-item" data-value="grains">
        Bread, Cereal, Rice, and Pasta
      </li>
      <li class="mdc-list-item" data-value="vegetables">
        Vegetables
      </li>
      <li class="mdc-list-item" data-value="fruit">
        Fruit
      </li>
    </ul>
  </div>
  <span class="mdc-floating-label">Pick a Food Group</span>
  <div class="mdc-line-ripple"></div>
</div>