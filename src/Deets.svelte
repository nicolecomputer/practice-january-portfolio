<div class="floating-window">
  <header>
    <h3>The-Deets.txt</h3>
  </header>
  <div class="row list">
    <h3>Tools</h3>
    <ol>
      <li>Svelte</li>
      <li>Typescript</li>
      <li>Vite</li>
    </ol>
  </div>
  <div class="row list">
    <h3>Features</h3>
    <ol>
      <li>Dark Mode</li>
      <li>Mobile</li>
      <li>Desktop</li>
    </ol>
  </div>
  <div class="row link">Github</div>
  <div class="row link">Website</div>
</div>

<style>
  .floating-window {
    background-color: white;
    box-shadow: 4px 3px 0 1px rgba(70, 70, 70, 0.8);
    border: 2px solid black;
  }

  header {
    font-family: monospace;
    background-color: #e4dfdf;
    padding: 12px 8px;
    border-bottom: 2px solid black;
    font-size: 12px;
  }

  .row {
    padding: 12px 8px;
    border-bottom: 2px solid black;
  }

  .list {
    border-bottom-width: 4px;
  }

  .list ol,
  .list li {
    display: inline;
    font-family: monospace;
  }

  .list h3 {
    margin-bottom: 8px;
  }

  .list ol {
    list-style-type: none;
    font-size: 10px;
  }

  li + li::before {
    content: "& ";
  }

  .link:hover {
    background-color: #f0f0f0;
    text-decoration: underline;
  }
</style>
