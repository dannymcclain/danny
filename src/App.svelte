<script>
  import Section from './Components/Section.svelte';
  import Link from './Components/Link.svelte';
  
  // let images = [
  //   { title: 'Danny',
  //     src: './images/Danny.svg'
  //   },
  //   { title: 'About',
  //     src: './images/About.svg'
  //   },
  //   { title: 'Design Utilities',
  //     src: './images/Projects.svg'
  //   },
  //   { title: 'Figma Plugins',
  //     src: './images/Plugins.svg'
  //   },
  //   { title: 'Currently',
  //     src: './images/Currently.svg'
  //   },
  //   { title: 'Elsewhere',
  //     src: './images/Elsewhere.svg'
  //   },
  //   { title: 'Good Stuff',
  //     src: './images/Good.svg'
  //   },
  // ]

  import { onMount } from 'svelte';
  // Maybe maybe add some randomness at some point?
  // function getRandomInt(max) {
  //   return Math.floor(Math.random() * max);
  // }
  // let randomNum =  getRandomInt(361)
	// let hue = randomNum;

  let hue = 0;

	onMount(() => {
		const interval = setInterval(() => {
			if (hue < 360) {
				hue++
				return hue
			} else if (hue = 360) {
				hue = 0
				return hue
			}
		}, 50);

		return () => {
			clearInterval(interval);
		};
	});
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
    color: rgba(0, 0, 0, .72);
    background: #fff;
    font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    padding: 0;
    margin: 0;
  }
  section {
    max-width: 1200px;
    padding: 40px;
    margin: 0 auto;
  }
  header {
    margin-bottom: 2rem;
  }
  main h1 {
    font-weight: 800;
    font-size: 2rem;
    line-height: 125%;
    letter-spacing: -0.04em;
  }
  footer {
    margin-top: 2rem;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  footer .icon-button:not(last-child){
    margin-right: 4rem;
  }
  .icon-button {
    font-weight: 500;
    font-size: 1.25rem;
    line-height: 100%;
    letter-spacing: -0.02em;
    color: #000000;
    opacity: 0.72;
    display: inline-flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    padding: 12px 16px;
    border: 2px solid #000000;
    border-radius: 100px;
  }
  .icon-button:hover {
    text-decoration: none;
    background: white;
  }
  .icon-button svg {
    margin-right: .5rem;
  }
  .title {
    transform: rotate(16deg);
    transition: transform 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  .title:hover {
    transform: rotate(-2deg);
  }
  .email {
    transform: rotate(-4deg);
    transition: transform 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  .email:hover {
    transform: rotate(4deg);
  }
  .instagram {
    transform: rotate(8deg);
    transition: transform 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  .instagram:hover {
    transform: rotate(-2deg);
  }
  .twitter {
    transform: rotate(-16deg);
    transition: transform 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  .twitter:hover {
    transform: rotate(-2deg);
  }
  @media only screen and (min-width: 760px) {
    section {
      padding: 120px;
    }
    header {
      margin-bottom: 4rem;
    }
    main h1 {
      font-size: 4rem;
    }
    footer {
      margin-top: 4rem;
    }
  }
</style>

<body style="background-color: hsl({hue}, 100%, 90%">
  <section>
    <header>
      <a href="/" class="title icon-button">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="12" cy="12" r="11" stroke="black" stroke-width="2"/>
        <circle cx="8.5" cy="9.5" r="1.5" fill="black"/>
        <circle cx="15.5" cy="9.5" r="1.5" fill="black"/>
        <path d="M7 14C7 14 8.5 17 12 17C15.5 17 17 14 17 14" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        Danny McClain</a>
    </header>
    <main>
      <h1>I’m a multidisciplinary designer currently working on design systems, interfaces, & icons.</h1>
    </main>
    <footer>
      <a href="mailto:dannyxmcclain@gmail.com" class="email icon-button"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="1" y="3" width="22" height="18" rx="4" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        <path d="M1 5L9.30931 12.5539C10.835 13.9409 13.165 13.9409 14.6907 12.5539L23 5" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        <path d="M9 12L2 20" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        <path d="M15 12L22 20" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        </svg>
        Email</a>
      <a href="https://instagram.com/dannymcclain" class="instagram icon-button"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M23 14.6V11.4C23 9.15979 23 8.03968 22.564 7.18404C22.1805 6.43139 21.5686 5.81947 20.816 5.43597C19.9603 5 18.8402 5 16.6 5H16L15.1094 3.6641C14.4163 2.62446 13.2495 2 12 2C10.7505 2 9.58369 2.62446 8.8906 3.6641L8 5H7.4C5.15979 5 4.03969 5 3.18404 5.43597C2.43139 5.81947 1.81947 6.43139 1.43597 7.18404C1 8.03968 1 9.15979 1 11.4V14.6C1 16.8402 1 17.9603 1.43597 18.816C1.81947 19.5686 2.43139 20.1805 3.18404 20.564C4.03969 21 5.15979 21 7.4 21H16.6C18.8402 21 19.9603 21 20.816 20.564C21.5686 20.1805 22.1805 19.5686 22.564 18.816C23 17.9603 23 16.8402 23 14.6Z" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        <circle cx="12" cy="13" r="4" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        </svg>
        Instagram</a>
      <a href="https://twitter.com/dannymcclain" class="twitter icon-button"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M1 9.4C1 7.15979 1 6.03968 1.43597 5.18404C1.81947 4.43139 2.43139 3.81947 3.18404 3.43597C4.03968 3 5.15979 3 7.4 3H16.6C18.8402 3 19.9603 3 20.816 3.43597C21.5686 3.81947 22.1805 4.43139 22.564 5.18404C23 6.03968 23 7.15979 23 9.4V10.6569C23 12.8434 23 13.9367 22.5841 14.7761C22.1954 15.5603 21.5603 16.1954 20.7761 16.5841C19.9367 17 18.8434 17 16.6569 17V17C16.4181 17 16.2987 17 16.1862 17.0263C16.0804 17.0511 15.9793 17.093 15.887 17.1503C15.7888 17.2112 15.7044 17.2956 15.5355 17.4645L13.1314 19.8686C12.7354 20.2646 12.5373 20.4627 12.309 20.5368C12.1082 20.6021 11.8918 20.6021 11.691 20.5368C11.4627 20.4627 11.2646 20.2646 10.8686 19.8686L8.46447 17.4645C8.29562 17.2956 8.2112 17.2112 8.11304 17.1503C8.02069 17.093 7.91962 17.0511 7.8138 17.0263C7.70132 17 7.58193 17 7.34315 17V17C5.15656 17 4.06327 17 3.22394 16.5841C2.43969 16.1954 1.80455 15.5603 1.41592 14.7761C1 13.9367 1 12.8434 1 10.6569V9.4Z" stroke="black" stroke-width="2" stroke-linejoin="round"/>
        <path d="M6 8H18" stroke="black" stroke-width="2" stroke-linecap="round"/>
        <path d="M6 12H14" stroke="black" stroke-width="2" stroke-linecap="round"/>
        </svg>
        Twitter</a>
    </footer>
  </section>
</body>