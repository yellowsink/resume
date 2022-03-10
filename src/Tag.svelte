<span class="txt"><slot/></span>
<span class="accent" />

<style>
  .txt {
    margin-bottom: var(--gap);
    display: inline-block;
  }

  .accent {
    display: inline-block;
    margin-left: calc(var(--gap) / 2);
    margin-right: calc(var(--gap) / 2);
    height: 1rem;

    border-left: solid 1px var(--accent);
  }
</style>