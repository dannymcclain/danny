<script>
  import Header from './Header.svelte'

  export let title = 'Section'
  export let src;
</script>

<style>
  div {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
  }
  section {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
    /* Gray 5 */
    background: #1A1A1E;
    border-radius: 0 0 20px 20px;
    width: 100%;
  }
  @media(min-width: 720px){
    section {
      padding: 40px;
    }
  }
</style>

<div>
  <Header title={title} {src} />
  <section>
    <slot></slot>
  </section>
</div>