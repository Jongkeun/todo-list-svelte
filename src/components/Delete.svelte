<script>
  export let onClick;
</script>

<style>
  button {
    float: right;
    background-color: transparent;
    border-width: 0;
    color: white;
    font-size: 30px;
    margin-left: auto;
  }
</style>

<button on:click={onClick}>X</button>
