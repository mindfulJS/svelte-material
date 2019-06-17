<script>
  // Material Design Card component

  export let imgSrc;
  export let imgTitle;
  export let imgDescription;
</script>

<!-- Card with photo -->
<div class="mdc-card my-card">
  <div class="mdc-layout-grid my-grid">
    <div class="mdc-layout-grid__inner">
      <div class="mdc-layout-grid__cell my-cell">
        <img class="mdc-image-list__image" alt="" src="{imgSrc}">
      </div>
      <p class="mdc-layout-grid__cell my-cell-content mdc-typography--body1">
        <b>{imgTitle}</b><br>
        {imgDescription}
      </p>
    </div>
  </div>
</div>

<style>
  .my-card {
    padding: 16px;
    margin: 16px;
    text-align: left;
  }
  .my-grid {
    width: 100%;
  }
  .my-cell {
    text-align: left;
  }
</style>