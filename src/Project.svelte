<script>
  //import AccentedHeader from "./AccentedHeader.svelte";
  import IconLink from "./IconLink.svelte";
  export let proj;
</script>

<div class="project-card">
  <!-- <AccentedHeader tag="h3">{proj.name}</AccentedHeader> -->
  <h3>{proj.name}</h3>
  <div class="info">{proj.info}</div>
  <IconLink icon="gh" href="https://github.com/{proj.github}"
    >{proj.github}</IconLink
  >
</div>

<style>
  .project-card {
    display: flex;
    flex-direction: column;
  }

  .info {
    margin-bottom: var(--gap);
    font-style: italic;
  }

  h3 {
    margin: 0;
  }
</style>
