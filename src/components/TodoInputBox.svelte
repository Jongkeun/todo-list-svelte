<script>
  export let addTodo;
  const onKeyPress = e => {
    if (e.charCode === 13 && e.target.value !== "") {
      addTodo(e.target.value);
      e.target.value = "";
    }
  };
</script>

<style>
  input {
    width: 100%;
    border-style: none;
  }
</style>

<input on:keypress={onKeyPress} />
