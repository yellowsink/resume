<script>
  import AccentedHeader from "./AccentedHeader.svelte";
  import Project from "./Project.svelte";
  import IconLink from "./IconLink.svelte";
  import Tag from "./Tag.svelte";
  import AboutMe from "./AboutMe.svelte";

  const links = [
    ["globe", "yellowsink.vercel.app", "https://yellowsink.vercel.app"],
    ["gh", "git.io/ysink", "https://git.io/ysink"],
    ["at", "yellowsink@riseup.net", "mailto:yellowsink@riseup.net"],
    ["discord", "Yellowsink#8156"],
    ["loc", "United Kingdom"],
    ["cake", "Aug 2006"]
  ]

  const projects = [
    {
      name: "Discord Command Palette",
      info: "Experience in React, JS, Sass, building a dev-facing local API",
      github: "yellowsink/discord-command-palette"
    },
    {
      name: "My Website",
      info: "Design & UI design - HTML & CSS, static site building (Astro)",
      github: "yellowsink/website-v2"
    },
    {
      name: "CLisp REPL",
      info: "Building a rich CLI in Node, Typescript, Lisp",
      github: "yellowsink/clisp-repl"
    },
    {
      name: "HLCC",
      info: "Node TS CLI dev tool for building small JS snippets - SWC (js transforms)",
      github: "yellowsink/hlcc"
    },
    {
      name: "Simian",
      info: "A JS monkey-patcher. Much experience with JS, classes, functions.",
      github: "yellowsink/simian"
    },
    {
      name: "Polystratum assets",
      info: "Some graphic design I did for a project that never went anywhere.",
      github: "PolyStratum/assets"
    }
  ]

  const tags = [
    ["Javascript", "Typescript", "F#", "Go", "C#", "zsh"],
    ["React", "Solid", "Svelte", "Avalonia"],
    ["Node", ".NET", "Fable", "Web"],
    ["esbuild", "Rollup", "Vite", "SWC"],
    ["vscode", "Rider"]
  ]
</script>

<div id="top-links">
  {#each links as link}
    <IconLink icon={link[0]} name={link[1]} href={link[2]} />
  {/each}
</div>

<div id="name">
  <AccentedHeader tag="h1" toLeft>Cain Atkinson</AccentedHeader>
  <div id="sub">Software and Frontend Developer</div>
</div>

<div id="projects">
  <AccentedHeader tag="h2">Projects</AccentedHeader>
  {#each projects as proj}
    <Project {proj} />
  {/each}
</div>

<div id="me">
  <AccentedHeader tag="h2">Me</AccentedHeader>
  <AboutMe />
</div>

<div id="tech">
  <AccentedHeader tag="h2" toLeft>Tech</AccentedHeader>
  {#each tags as tagGroup}
    <div>
      {#each tagGroup as tag}
        <Tag>{tag}</Tag>
      {/each}
    </div>
  {/each}
</div>