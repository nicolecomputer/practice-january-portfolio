<script lang="ts">
  import Deets from "./Deets.svelte";

  const { url, description, tools, features, links, title } = $props();
</script>

<div id="project">
  <div id="left">
    <iframe src={url} id="gallery-slot" title="Project Preview"></iframe>
  </div>
  <div id="right">
    <h1>{title}</h1>
    <hr />
    <article>
      <p>
        {description}
      </p>
    </article>
    <Deets {tools} {features} githubSrcUrl={links.github} websiteUrl={url} />
  </div>
</div>

<style>
  #project {
    flex: 1;
    flex-direction: row;
    padding: 16px;
    gap: 3%;
  }

  #left {
    width: 60%;
  }

  #gallery-slot {
    width: 100%;
    height: 100%;
    border: 3px solid black;
    background-color: white;
    box-shadow: 4px 4px 0px rgba(122, 122, 122, 0.5);
  }

  #right {
    padding-top: 10px;
    flex-direction: column;
    flex: 1;
  }

  h1 {
    font-size: 48px;
  }

  hr {
    width: 100%;
  }

  article {
    flex: 1;
  }
</style>
