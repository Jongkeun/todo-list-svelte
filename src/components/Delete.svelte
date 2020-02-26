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
    padding: 9px 10px;
    cursor: pointer;
  }
</style>

<button on:click={onClick}>X</button>
