<script>
  export let icon, name, href;
</script>

<a {href} target="_blank">
  <img src="/svg/{icon}.svg" alt="{icon}">
  {name}
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

  img { width: 1.25rem; }
</style>