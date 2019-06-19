<script>
  // Material Design Tab Bar component

  import { onMount } from "svelte";
  import * as mdc from "material-components-web";

  onMount(() => {
    // Initialise Material Components Web
    mdc.autoInit();
  });
</script>

<!-- Tab Bar -->
<div class="mdc-tab-bar" role="tablist" data-mdc-auto-init="MDCTabBar">
  <div class="mdc-tab-scroller">
    <div class="mdc-tab-scroller__scroll-area">
      <div class="mdc-tab-scroller__scroll-content">
        <button class="mdc-tab mdc-tab--active" role="tab" aria-selected="true" tabindex="0">
          <span class="mdc-tab__content">
            <span class="mdc-tab__text-label">Tab One</span>
          </span>
          <span class="mdc-tab-indicator mdc-tab-indicator--active">
            <span class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span>
          </span>
          <span class="mdc-tab__ripple"></span>
        </button>
        <button class="mdc-tab" role="tab" aria-selected="true">
          <span class="mdc-tab__content">
            <span class="mdc-tab__text-label">Tab Two</span>
          </span>
          <span class="mdc-tab-indicator">
            <span class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span>
          </span>
          <span class="mdc-tab__ripple"></span>
        </button>
        <button class="mdc-tab" role="tab" aria-selected="true">
          <span class="mdc-tab__content">
            <span class="mdc-tab__text-label">Tab Three</span>
          </span>
          <span class="mdc-tab-indicator">
            <span class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span>
          </span>
          <span class="mdc-tab__ripple"></span>
        </button>
      </div>
    </div>
  </div>
</div>