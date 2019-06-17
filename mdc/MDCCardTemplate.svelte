<script>
  // Card template
  import MDCCard from "/mdc/MDCCard.svelte";

  export let imgSrc;
  export let imgTitle;
  export let imgDescription;
</script>

<!-- Card with photo -->
<MDCCard {imgSrc} {imgTitle} {imgDescription} />
