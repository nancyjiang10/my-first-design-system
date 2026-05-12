<script>
  let { children } = $props();
</script>

<div class="row">
  {@render children()}
</div>

<style>
  .row {
    margin: var(--spacing-lg) 0;
    display: flex;
    gap: var(--spacing-sm);
    flex-wrap: wrap;
    justify-content: center;
  }

  .row > :global(*) {
    flex: 1;
    min-width: 200px;
    max-width: 300px;
  }
</style>