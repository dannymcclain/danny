<script>
  export let src;
</script>

<style>
  a {
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    text-decoration: none;
    padding: 12px 20px;
    /* Gray 3 */
    border: 2px solid #333335;
    box-sizing: border-box;
    border-radius: 100px;
    background: transparent;

    transition: background 150ms linear, color 100ms linear, border 150ms linear;
  }

  a:hover {
    color: #1A1A1E;
    border: 2px solid #fff;
    background: #fff;
  }
</style>

<a href={src} target="_blank"><slot></slot></a>