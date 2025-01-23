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
    content: "& ";
  }

  .link:hover {
    background-color: #daebff;
    text-decoration: underline;
    cursor: pointer;
  }
</style>
