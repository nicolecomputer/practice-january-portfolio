<script lang="ts">
  const { tools, features, githubSrcUrl, websiteUrl } = $props();
</script>

<div class="floating-window">
  <header>
    <h3>The-Deets.txt</h3>
  </header>
  <div class="row list">
    <h3>Tools</h3>
    <ol>
      {#each tools as tool}
        <li>{tool}</li>
      {/each}
    </ol>
  </div>
  <div class="row list">
    <h3>Features</h3>
    <ol>
      {#each features as feature}
        <li>{feature}</li>
      {/each}
    </ol>
  </div>
  <div class="row link">
    <a href={githubSrcUrl} target="_blank">Github</a>
  </div>
  <div class="row link">
    <a href={websiteUrl} target="_blank">Website</a>
  </div>
</div>

<style>
  .floating-window {
    background-color: white;
    box-shadow: 4px 3px 0 1px rgba(70, 70, 70, 0.8);
    border: 2px solid black;
  }

  header {
    background-color: #dce1e4;
    padding: 12px 8px;
    border-bottom: 2px solid black;
    font-size: 10px;
  }

  .row {
    padding: 12px 8px;
    border-bottom: 2px solid black;
    font-size: 14px;
  }

  .list {
    border-bottom-width: 4px;
  }

  .list ol,
  .list li {
    display: inline;
  }

  .list h3 {
    margin-bottom: 8px;
    font-size: 14px;
  }

  .list ol {
    list-style-type: none;
    font-size: 12px;
  }

  li + li::before {
    content: ", ";
  }

  a {
    text-decoration: none;
    color: black;
  }

  a:visited {
    color: black;
  }

  .link:hover {
    background-color: #daebff;
    text-decoration: underline;
    cursor: pointer;
  }
</style>
