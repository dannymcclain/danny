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
  span {
    display: inline-block;
  }
</style>

<main>
  <!-- {#if number === 0}
    <p
      in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
      out:fly={{ y: -20, duration: 400, easing: backInOut }}>
      Cool interfaces
    </p>
  {:else if number === 1}
    <p
      in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
      out:fly={{ y: -20, duration: 400, easing: backInOut }}>
      Snazzy apps
    </p>
  {:else if number === 2}
    <p
      in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
      out:fly={{ y: -20, duration: 400, easing: backInOut }}>
      Neat iconsets
    </p>
  {:else if number === 3}
    <p
      in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
      out:fly={{ y: -20, duration: 400, easing: backInOut }}>
      Boss utilities
    </p>
  {/if} -->
  <p>
    Things I make:
    {#if number === 0}
      <span
        in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
        out:fly={{ y: -20, duration: 400, easing: backInOut }}>
        Cool interfaces
      </span>
    {:else if number === 1}
      <span
        in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
        out:fly={{ y: -20, duration: 400, easing: backInOut }}>
        Snazzy apps
      </span>
    {:else if number === 2}
      <span
        in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
        out:fly={{ y: -20, duration: 400, easing: backInOut }}>
        Neat iconsets
      </span>
    {:else if number === 3}
      <span
        in:fly={{ y: 20, duration: 400, delay: 400, easing: backInOut }}
        out:fly={{ y: -20, duration: 400, easing: backInOut }}>
        Boss utilities
      </span>
    {/if}
  </p>
</main>
