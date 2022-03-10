<script>
  export let toLeft = false;
  export let tag;
</script>

<!-- I am so sorry for this affront to god -->

{#if tag == "h3"}
  <h3>
    {#if toLeft}
      <div class="left accent-line" />
      <slot />
    {:else}
      <slot />
      <div class="right accent-line" />
    {/if}
  </h3>
{:else if tag == "h2"}
  <h2>
    {#if toLeft}
      <div class="left accent-line" />
      <slot />
    {:else}
      <slot />
      <div class="right accent-line" />
    {/if}
  </h2>
{:else}
  <h1>
    {#if toLeft}
      <div class="left accent-line" />
      <slot />
    {:else}
      <slot />
      <div class="right accent-line" />
    {/if}
  </h1>
{/if}

<style>
  h1, h2, h3 {
    display: flex;
    gap: var(--gap);
    align-items: center;
  }

  .accent-line {
    width: 7.5rem;
    border-top: solid 2px;
    border-image: linear-gradient(to var(--direction), var(--accent), transparent) 1;
    align-self: center;
  }

  .accent-line.left { --direction: left; }
  .accent-line.right { --direction: right; }
</style>