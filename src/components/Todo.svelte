<script>
  import Checkbox from "./Checkbox";
  import Delete from "./Delete";

  export let todo;
</script>

<style>
  div {
    display: flex;
    height: 100px;
    width: 90%;
    margin: 4px 0;
    font-size: 2.5em;
    color: white;
    text-align: center;
    border-radius: 30px;
    border: 1px solid white;
    padding: 10px;
  }
</style>

<div>
  <Checkbox {todo} />
  <Delete />
</div>
