<script>
  // Card for each item of the Json list
  import MDCCard from "./mdc/MDCCardTemplate.svelte";

  export let photo;
</script>

<!-- Card with photo -->
<MDCCard imgSrc="{photo.download_url}" imgTitle="{photo.author}" imgDescription="description" />
