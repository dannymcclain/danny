<script>
  import Header from './Header.svelte'

  export let sectionTitle = 'Section'
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
    padding: 40px;
    /* Gray 5 */
    background: #1A1A1E;
    border-radius: 0 0 20px 20px;
    width: 100%;
  }
</style>

<div>
  <Header title={sectionTitle} {src} />
  <section>
    <slot></slot>
  </section>
</div>