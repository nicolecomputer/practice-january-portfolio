<script lang="ts">
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Deets from "./Deets.svelte";
</script>

<div id="shell">
  <main>
    <div id="left">
      <div id="placeholder"></div>
    </div>
    <div id="right">
      <h1>Quiz</h1>
      <hr />
      <article>
        <p>
          Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos
          facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus
          ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus
          est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem
          dapibus mauris nostra phasellus platea ultricies ac. Potenti purus
          vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra
          congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus
          phasellus.
        </p>
      </article>
      <Deets />
    </div>
  </main>
  <nav>
    <h2>coming soon nav</h2>
  </nav>
</div>

<style>
  #shell {
    height: 100%;
    max-height: 100vh;
    aspect-ratio: 4/3;
  }

  main {
    flex: 1;
    flex-direction: row;
    padding: 16px;
    gap: 3%;
  }

  nav {
    height: 60px;
    align-items: center;
    justify-content: center;
    color: gray;
    font-size: 10px;
  }

  #left {
    width: 70%;
  }

  #placeholder {
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
