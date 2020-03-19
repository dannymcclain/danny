<script>
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";
  import { cubicOut } from "svelte/easing";
  import { backInOut } from "svelte/easing";

  let number = 0;

  onMount(() => {
    const interval = setInterval(() => {
      if (number < 3) {
        number += 1;
      } else {
        number = 0;
      }
    }, 2000);

    return () => clearInterval(interval);
  });
</script>

<style>
  :global(body) {
    color: #808080;
    background: #111;
    font-family: "SFMono-Regular", Menlo, Consolas, "Liberation Mono", Courier,
      monospace;
    font-size: 14px;
    line-height: 24px;
  }
  main {
    padding: 40px 20px;
  }
  header {
    margin-bottom: 40px;
  }
  section {
    margin-bottom: 40px;
  }
  .projects {
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-items: flex-start;
  }
  .project {
    margin-right: 0;
    margin-bottom: 40px;
  }
  .project:last-child {
    margin-bottom: 0;
  }

  h1,
  h2 {
    font-size: 14px;
    line-height: 24px;
    color: #fff;
    font-weight: bold;
  }
  h1 {
    position: relative;
  }
  h2::after {
    content: "-";
    font-weight: 400;
    color: #fff;
    display: block;
  }
  h1 span {
    position: absolute;
    top: 0;
    left: 20ch;
    display: inline-flex;
    flex-direction: row-reverse;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-items: center;
  }
  h1 span img {
    margin-right: 1ch;
  }
  p {
    margin-bottom: 12px;
  }
  p:last-child {
    margin-bottom: 0;
  }
  ul {
    list-style: none;
  }
  a {
    color: inherit;
    text-decoration: underline;
  }
  a:hover {
    color: #fff;
  }
  @media (min-width: 700px) {
    main {
      padding: 40px;
    }
    header,
    section {
      max-width: 600px;
      /* margin: 0 auto 40px; */
    }
    .projects {
      flex-direction: row;
    }
    .project {
      margin-right: 80px;
    }
    .project:last-child {
      margin-right: 0;
    }
  }
</style>

<main>
  <header>
    <h1>
      Danny McClain makes
      {#if number === 0}
        <span
          in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
          out:fly={{ y: -20, duration: 400, easing: backInOut }}>
          apps.
          <img src="./images/icon-phone.svg" alt="phone icon" />
        </span>
      {:else if number === 1}
        <span
          in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
          out:fly={{ y: -20, duration: 400, easing: backInOut }}>
          interfaces.
          <img src="./images/icon-laptop.svg" alt="laptop icon" />
        </span>
      {:else if number === 2}
        <span
          in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
          out:fly={{ y: -20, duration: 400, easing: backInOut }}>
          icons.
          <img src="./images/icon-icon.svg" alt="icon icon" />
        </span>
      {:else if number === 3}
        <span
          in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
          out:fly={{ y: -20, duration: 400, easing: backInOut }}>
          utilities.
          <img src="./images/icon-code.svg" alt="code icon" />
        </span>
      {/if}
    </h1>
  </header>
  <section>
    <h2>About</h2>
    <p>
      I’m a digital product designer who likes to build stuff too. I’m always
      learning because learning is fun.
    </p>
    <p>
      I like designing interfaces, systems, and icons. I’m also weirdly
      passionate about efficiency and organization so I like to design and build
      tools, apps, and plugins that speed up my workflow.
    </p>
  </section>
  <section class="projects">
    <div class="project">
      <h2>Misc. Utilities</h2>
      <ul>
        <li>
          <a href="https://ratio-calc.netlify.com">Ratio</a>
        </li>
        <li>
          <a href="https://pixelgrids.netlify.com">Pixel Grids</a>
        </li>
        <li>
          <a href="https://grid-calc.netlify.com">Grid Calc</a>
        </li>
      </ul>
    </div>
  </section>
  <section>
    <h2>Currently</h2>
    <p>
      I’m currently a senior product designer at
      <a href="https://smiledirectclub.com">SmileDirectClub</a>
      working on digital experiences that help people get a smile they’re proud
      of.
    </p>
  </section>
  <section>
    <h2>Links</h2>
    <ul>
      <li>
        <a href="https://dribbble.com/dannymcclain">Dribbble</a>
      </li>
      <li>
        <a href="https://github.com/dannymcclain">Github</a>
      </li>
      <li>
        <a href="https://twitter.com/dannymcclain">Twitter</a>
      </li>
      <li>
        <a href="https://www.figma.com/@dannymcclain">Figma</a>
      </li>
      <li>
        <a href="mailto:dannyxmcclain@gmail.com">Email</a>
      </li>
    </ul>
  </section>
</main>
