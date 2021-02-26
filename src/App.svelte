<script>
  import Section from './Components/Section.svelte';
  import Link from './Components/Link.svelte';
  
  let images = [
    { title: 'Danny',
      src: './images/Danny.svg'
    },
    { title: 'About',
      src: './images/About.svg'
    },
    { title: 'Design Utilities',
      src: './images/Projects.svg'
    },
    { title: 'Figma Plugins',
      src: './images/Plugins.svg'
    },
    { title: 'Currently',
      src: './images/Currently.svg'
    },
    { title: 'Elsewhere',
      src: './images/Elsewhere.svg'
    },
    { title: 'Good Stuff',
      src: './images/Good.svg'
    },
  ]
</script>

<style>
  @import url('https://rsms.me/inter/inter.css');

  /* Mini Reset */
  :global(*),
  :global(*::after),
  :global(*::before) {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

  :global(body) {
    color: #8E8E92;
    background: #111112;
    font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 28px;
    letter-spacing: -0.01em;
    padding: 0;
    margin: 0;
  }

  main {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 20px;
    gap: 20px;
    padding: 20px;
    max-width: 1120px;
    margin: 0 auto;
  }
  
  h1,
  h2 {
    font-weight: bold;
    font-size: 16px;
    line-height: 16px;
    color: #FFFFFF;
    margin-bottom: 20px;
  }
  p {
    margin-bottom: 20px;
  }
  p:last-child {
    margin-bottom: 0;
  }
  .mt {
    margin-top: 20px;
  }
  ul {
    list-style: none;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
  }
  li {
    margin: 0 20px 20px 0;
    }
  /* li:not(:last-child) {
    margin: 0 20px 20px 0;
    } */
  
  @media (min-width: 840px) {
    main {
      grid-template-columns: 1fr 1fr;
      padding: 40px;
      grid-gap: 40px;
      gap: 40px;
    }
  }
</style>

<main>
  <Section title="Danny McClain" src="./images/Danny.svg">
    <h1>Danny McClain</h1>
    <p>I’m  a designer and developer homesteading with my wife and son in a little house out in the country.</p>
  </Section>

  <Section title="About" src="./images/About.svg">
    <h2>About</h2>
    <p>I specialize in designing interfaces, systems, and icons. I like building simple, humble tools to help me work faster and smarter.</p>
    <p>My hope is to create things that make designers’ and developers’ lives a little bit better.</p>
  </Section>
  
  <Section title="Design Utilities" src="./images/Projects.svg">
    <h2>Design Utilities</h2>
    <p>A few projects from the archives.</p>
    <ul>
      <li><Link src="https://ratio.dannymcclain.com">Ratio ↗</Link></li>
      <li><Link src="https://gridfinder.dannymcclain.com/">Grid Finder ↗</Link></li>
      <li><Link src="https://gridcalc.dannymcclain.com/">Grid Calc ↗</Link></li>
    </ul>
  </Section>

  <Section title="Figma Plugins" src="./images/Plugins.svg">
    <h2>Figma Plugins</h2>
    <Link src="https://www.figma.com/community/plugin/917796239623005893/Fitter">Fitter ↗</Link>
    <p class="mt">More plugins in the works.</p>
  </Section>

  <Section title="Currently" src="./images/Currently.svg">
    <h2>Currently</h2>
    <p>I’m currently working on design systems.</p>
    <Link src="https://smiledirectclub.com/">SmileDirectClub ↗</Link>
  </Section>
  
  <Section title="Elsewhere" src="./images/Elsewhere.svg">
    <h2>Elsewhere</h2>
    <ul>
      <li><Link src="https://dribbble.com/dannymcclain">Dribbble ↗</Link></li>
      <li><Link src="https://github.com/dannymcclain">Github ↗</Link></li>
      <li><Link src="https://twitter.com/dannymcclain">Twitter ↗</Link></li>
      <li><Link src="https://www.figma.com/@dannymcclain">Figma Community ↗</Link></li>
      <li><Link src="mailto:dannyxmcclain@gmail.com">Email ↗</Link></li>
    </ul>
    <p>Thanks for stopping by.</p>
  </Section>

  <Section title="Good Stuff" src="./images/Good.svg">
    <h2>Good Stuff</h2>
    <p>These are not sponsored or affiliate links. Just some things I personally enjoy.</p>
    <ul>
      <li><Link src="https://www.figma.com">Figma ↗</Link></li>
      <li><Link src="https://www.sleepwithmepodcast.com">Sleep with Me Podcast ↗</Link></li>
      <li><Link src="https://bear.app">Bear ↗</Link></li>
      <li><Link src="https://1password.com">1Password ↗</Link></li>
    </ul>
  </Section>
</main>