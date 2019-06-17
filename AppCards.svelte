<script>
  // Json part
  import { fade } from "svelte/transition";
  import AppCardsButton from "./AppCardsButton.svelte";
  import AppCardsList from "./AppCardsList.svelte";

  import { showData } from "./stores.js";
</script>

<!-- Button to load Json Data-->
<AppCardsButton />

<!-- Json Data List -->
{#if $showData}
  <div transition:fade>
    <AppCardsList />
  </div>
{/if}
