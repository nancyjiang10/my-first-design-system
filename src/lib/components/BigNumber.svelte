
<script>
  let { number, label, footnote } = $props();
</script>

<div class="big-number">
  <span class="number">{number}</span>
  <span class="label">{label}</span>
  {#if footnote}
    <span class="footnote">{footnote}</span>
  {/if}
</div>

<style lang="scss">
  @use '../styles' as *;
  .big-number {
    text-align: center;
    padding: var(--spacing-md);
    background-color: var(--color-accent);
    color: var(--color-white);
    border-radius: 8px;
  }

  .number {
    display: block;
    font-size: var(--font-size-4xl);
    font-weight: bold;
    color: var(--color-white);
    line-height: var(--leading-tight);
  }

  .label {
    display: block;
    font-size: var(--font-size-base);
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin-top: var(--spacing-xs);
  }

    .footnote {
    display: block;
    font-size: var(--font-size-sm);
    color: var(--color-white);
    margin-top: var(--spacing-xs);
    font-style: italic;
  }


  @include mobile {
    .big-number {
      padding: var(--spacing-sm);
    }

    .number {
      font-size: var(--font-size-3xl);
    }

    .label {
      margin-top: var(--spacing-xs);
      font-size: var(--font-size-sm);
    }

    .footnote {
      margin-top: var(--spacing-xs);
      font-size: var(--font-size-xs);
    }
  }
</style>