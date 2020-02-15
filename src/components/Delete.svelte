<script>
  export let onClick;
</script>

<style>
  button {
    padding: 0 10px 0 0;
    float: right;
    background-color: transparent;
    border-width: 0;
    color: white;
    font-size: 30px;
    margin-left: auto;
    cursor: pointer;
  }
</style>

<button on:click={onClick}>X</button>
