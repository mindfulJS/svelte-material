<script>
  // Json part
  import { fade } from "svelte/transition";
  import AppJsonButton from "./AppJsonButton.svelte";
  import AppJsonList from "./AppJsonList.svelte";

  import { showData } from "./stores.js";
</script>

<!-- Button to load Json Data-->
<AppJsonButton />

<!-- Json Data List -->
{#if $showData}
  <div transition:fade>
    <AppJsonList />
  </div>
{/if}
