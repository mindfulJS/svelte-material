<script>
  // Button template
  import MDCButton from "/mdc/MDCButton.svelte";

  export let buttonText;
  export let onClickFunction;
</script>

<!-- Button -->
<MDCButton {buttonText} {onClickFunction} />