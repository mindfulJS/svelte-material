<script>
  // Card for each item of the Json list
  import MDCCard from "./mdc/MDCCard.svelte";

  export let photo;
</script>

<!-- Card with photo -->
<MDCCard imgUrl="{photo.download_url}" title="{photo.author}" />
