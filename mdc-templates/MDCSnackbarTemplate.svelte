<script>
	// Snackbar template
	import MDCSnackbar from "/mdc/MDCSnackbar.svelte";
	import { onMount } from "svelte";

	export let snackbarMessage;

	onMount(async () => {
	  // Open Snackbar when something has loaded
	  //document.querySelector(".mdc-snackbar").MDCSnackbar.open();
	});
</script>

<!-- Snackbar -->
<MDCSnackbar {snackbarMessage} />