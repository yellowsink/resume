<script>
  export let icon, href;
</script>

<a {href} target="_blank">
  <div>
    <img src="/svg/{icon}.svg" alt="{icon}">
  </div>
  <slot />
</a>

<style>
  a {
    color: var(--accent);
    text-decoration: unset;
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: var(--gap);
  }

  div {
    width: 1.25rem;
    height: 1.25rem;
    display: flex;
    justify-content: center;
  }

  /* img { height: 100%; } */
</style>