<script>
	// List of items for Json part
	import { onMount } from "svelte";
	import AppJsonListCard from "./AppJsonListCard.svelte";
	import MDCSnackbar from "./mdc/MDCSnackbarTemplate.svelte";
	let photos = [];

	// Get Json Data (photos)
	onMount(async () => {
	  const res = await fetch(`https://picsum.photos/v2/list`);
	  photos = await res.json();
	  //console.log(photos);
	  photos = shuffle(photos);
	  // Open Snackbar when data is loaded
	  document.querySelector(".mdc-snackbar").MDCSnackbar.open();
	});

	//Shuffle photos
	function shuffle(array) {
	  let currentIndex = array.length,
	    temporaryValue,
	    randomIndex;

	  // While there remain elements to shuffle...
	  while (0 !== currentIndex) {
	    // Pick a remaining element...
	    randomIndex = Math.floor(Math.random() * currentIndex);
	    currentIndex -= 1;

	    // And swap it with the current element.
	    temporaryValue = array[currentIndex];
	    array[currentIndex] = array[randomIndex];
	    array[randomIndex] = temporaryValue;
	  }

	  return array;
	}
</script>

<!-- List of photos -->
<div>
	{#each photos as photo (photo.id)}
		<AppJsonListCard {photo} />
	{:else}
			<!-- this block renders when photos.length === 0 -->
		<p>Loading...</p>
	{/each}

	<MDCSnackbar snackbarMessage="Data loaded successfully"/>
</div>
