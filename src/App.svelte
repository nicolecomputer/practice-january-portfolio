<script lang="ts">
  import ProjectScreen from "./ProjectScreen/ProjectScreen.svelte";

  const projects = [
    {
      title: "Basic Todo",
      url: "https://practice-todo-app.lion.computer",
      description:
        "Call it humble beginnings. My fingers are still cold and the challenge is to build a TODO app. Todo app done but this is worth another swing.",
      tools: ["React", "Typescript"],
      features: ["desktop"],
      links: {
        github: "https://github.com/nicolecomputer/practice-todo-app",
      },
    },
    {
      title: "Tweet Layout",
      url: "https://practice-tweet-layout.lion.computer",
      description: "Challenge: build a tweet component.",
      tools: ["React", "Typescript", "Vite"],
      features: ["desktop", "mobile"],
      links: {
        github: "https://github.com/nicolecomputer/practice-tweet-layout",
      },
    },
    {
      title: "Temperature Converter",
      url: "https://practice-temperature-converter.lion.computer",
      description:
        "It's cold out and not all my friends use the same temperature system- build a temperature converter. This was meant to be a quick function-only question but it needed to have a frontend",
      tools: ["React", "Typescript", "Vite", "Pico.css"],
      features: ["desktop"],
      links: {
        github:
          "https://github.com/nicolecomputer/practice-temperature-converter",
      },
    },
    {
      title: "Classlist Toy",
      url: "https://practice-classlist.lion.computer",
      description:
        "An API exploration that grew into a little toy. The rectangle changes colors, rotates, scales, and skews!",
      tools: ["Pure JS", "Static HTML/CSS/JS"],
      features: ["desktop"],
      links: {
        github: "https://github.com/nicolecomputer/classlist-toy",
      },
    },
    {
      title: "Star Rating",
      url: "https://practice-star-rating.lion.computer",
      description:
        "What's the rating on this book, film, or sweatshirt? Star rating components are everywhere. This component lets a user rate but also lets them add more stars if their rating system isn't a 1-5 kind-of-deal.",
      tools: ["React", "Typescript", "Vite"],
      features: ["desktop", "mobile"],
      links: {
        github: "https://github.com/nicolecomputer/practice-star-rating",
      },
    },
    {
      title: "Progress Bar",
      url: "https://practice-progress-bar.lion.computer",
      description:
        "A progress bar! I did the design for this one and started to get really into buttons. There are some small niceties like the percentage hiding when the bar gets small.",
      tools: ["React", "Typescript", "Vite"],
      features: ["desktop", "mobile", "dark mode"],
      links: {
        github: "https://github.com/nicolecomputer/practice-progress-bar",
      },
    },
    {
      title: "AC Friend Level Up",
      url: "https://practice-animal-crossing.lion.computer",
      description:
        "We got a big snow and I got into playing Animal Crossing Pocket Camp. I loved all the little moments of delight and wanted to recreate one of the screens from the game.",
      tools: ["Svelte", "Typescript", "Vite"],
      features: ["mobile"],
      links: {
        github: "https://github.com/nicolecomputer/practice-ac-friend-level",
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
      title: "Notes Page Redesign",
      url: "https://notes.nicole.computer",
      description:
        "A redesign of my notes website with a theme that feels like me. I did the design for this!",
      tools: ["Quartz", "HTML", "CSS"],
      features: ["desktop", "mobile"],
      links: {
        github: "https://github.com/nicolecomputer/quartz",
      },
    },
    {
      title: "Quiz",
      url: "https://practice-quiz.lion.computer",
      description:
        "A bigger project to build out a quiz app. Has a start of task card, quiz, and end of task/stats card.",
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
        "You are here! You have just used this app to flip through the things I've made in January 2025",
      tools: ["Svelte", "Typescript", "Vite"],
      features: ["desktop"],
      links: {
        github: "https://github.com/nicolecomputer/practice-january-portfolio",
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
