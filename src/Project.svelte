<script>
  //import AccentedHeader from "./AccentedHeader.svelte";
  import IconLink from "./IconLink.svelte";
  export let proj;
</script>

<div class="project-card">
  <!-- <AccentedHeader tag="h3">{proj.name}</AccentedHeader> -->
  <h3>{proj.name}</h3>
  <div class="info">{proj.info}</div>
  <IconLink
    icon="gh"
    name={proj.github}
    href="https://github.com/{proj.github}"
  />
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
</style>
