<script lang="ts">
  import ProjectScreen from "./ProjectScreen/ProjectScreen.svelte";

  const projects = [
    {
      title: "Basic Todo",
      url: "https://practice-todo-app.lion.computer",
      description:
        "Call it humble beginnings. My fingers are still cold and the challenge is to build a TODO app. Todo app done but this is worth another swing.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "Tweet Layout",
      url: "https://practice-tweet-layout.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "Temperature Converter",
      url: "https://practice-temperature-converter.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "Classlist Toy",
      url: "https://practice-classlist.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "Star Rating",
      url: "https://practice-star-rating.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "Progress Bar",
      url: "https://practice-progress-bar.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "AC Friend Level Up",
      url: "https://practice-animal-crossing.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["-"],
      features: ["-"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "Digital Clock",
      url: "https://practice-digital-clock.lion.computer",
      description:
        "The challenge? Display a digital clock without ever typing the numbers. No fonts allowed! The solution? Carefully placed div's and some styling. Viola! This project made careful use of React's useEffect hook to update the current time state.",
      tools: ["React", "Typescript", "Vite"],
      features: ["desktop", "mobile"],
      links: {
        github: "https://github.com/nicolecomputer/practice-digital-clock",
      },
    },
    {
      title: "Quiz",
      url: "https://practice-quiz.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["Svelte", "Typescript", "Vite"],
      features: ["dark mode", "desktop", "mobile"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
    {
      title: "January Portfolio",
      url: "https://practice-portfolio.lion.computer",
      description:
        "Lorem ipsum odor amet, consectetuer adipiscing elit. Himenaeos facilisi ultrices curabitur fringilla pretium iaculis ad. Maximus ligula faucibus ex habitant eros. Cubilia id nec tempor mattis tempus est non. Ullamcorper mollis eleifend; taciti netus class platea. Lorem dapibus mauris nostra phasellus platea ultricies ac. Potenti purus vehicula mus ante libero aliquet. Quam velit vitae feugiat viverra congue magnis conubia. Malesuada aenean nec dictumst; aliquam maximus phasellus.",
      tools: ["Svelte", "Typescript", "Vite"],
      features: ["dark mode", "desktop", "mobile"],
      links: {
        github: "https://github.com/nicolecomputer/practice-quiz",
      },
    },
  ];

  let activeProjectIndex = $state(0);
  let activeProject = $derived(projects[activeProjectIndex]);

  function prevProject() {
    activeProjectIndex = Math.max(activeProjectIndex - 1, 0);
  }

  function nextProject() {
    activeProjectIndex = Math.min(activeProjectIndex + 1, projects.length - 1);
  }

  function handleKeydown(event: KeyboardEvent) {
    if (event.key === "ArrowRight") {
      nextProject();
    } else if (event.key === "ArrowLeft") {
      prevProject();
    }
  }
</script>

<svelte:window on:keydown={handleKeydown} />

<div id="shell">
  <main>
    <ProjectScreen
      title={activeProject.title}
      url={activeProject.url}
      description={activeProject.description}
      tools={activeProject.tools}
      features={activeProject.features}
      links={activeProject.links}
    />
  </main>
  <nav>
    <button onclick={prevProject} disabled={activeProjectIndex === 0}>
      Prev
    </button>
    <div id="indicators">
      {#each Array(projects.length) as _, i}
        <div
          class={[
            "nav-indicator",
            i === activeProjectIndex ? "active" : "inactive",
          ]}
        ></div>
      {/each}
    </div>
    <button
      onclick={nextProject}
      disabled={activeProjectIndex === projects.length - 1}
    >
      Next
    </button>
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
  }

  nav {
    height: 60px;
    align-items: center;
    justify-content: center;
    color: gray;
    font-size: 10px;
    flex-direction: row;
    justify-content: space-between;
  }

  nav button {
    background-color: black;
    color: white;
    border: 0px solid black;
    box-shadow: 2px 3px 0 rgb(169, 169, 169);
    padding: 8px 12px;
    font-family: Fira;

    transition:
      opacity 200ms ease-in-out,
      background-color 100ms,
      transform 200ms;
  }
  nav button:disabled {
    opacity: 0%;
  }

  nav button:hover {
    background-color: rgb(32, 62, 83);
  }

  nav button:active {
    transform: translateY(3px) translateX(2px);
    box-shadow: none;
    background-color: rgb(65, 65, 65);
  }

  #indicators {
    flex-direction: row;
    gap: 4px;
  }

  nav .nav-indicator {
    height: 10px;
    width: 10px;
    border-radius: 5px;
    background-color: black;
    border: 2px solid black;

    transform-origin: center;

    transition: width 500ms 200ms;
  }

  nav .active {
    background-color: white;
    width: 30px;
    margin: 0 4px;
  }
</style>
