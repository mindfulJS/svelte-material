<script>
  // Button for Json part
  import { showData } from "./stores.js";
  import MDCButton from "./mdc-templates/MDCButtonTemplate.svelte";

  function reload() {
    toggle();
    setTimeout(function() {
      toggle();
    }, 500);
  }

  function toggle() {
    showData.update(value => !value);
  }
</script>

<!-- Button -->
<MDCButton buttonText="Reload new photos" onClickFunction={reload} />