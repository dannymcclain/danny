<script>
  export let src;
  export let title;
</script>

<style>
  section {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 12px 16px;
    background: #232326;
    border-radius: 20px 20px 0 0;
  }
</style>

<section>
  <img {src} alt="{title} icon" />
</section>