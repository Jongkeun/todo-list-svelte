<script>
  import Checkbox from "./Checkbox";
  import Delete from "./Delete";

  export let todo;
  export let deleteTodo;
  export let updateTodo;

  const deleteClick = function(e) {
    deleteTodo(todo.id);
  };

  const updateClick = () => {
    updateTodo(todo.id);
  };
</script>

<style>
  div {
    display: flex;
    height: 40px;
    width: 90%;
    margin: 4px 0;
    font-size: 2em;
    color: white;
    text-align: center;
    border-radius: 30px;
    border: 1px solid white;
    padding: 10px;
  }
</style>

<div>
  <Checkbox
    content={todo.content}
    onClick={updateClick}
    checked={todo.isDone} />
  <Delete onClick={deleteClick} />
</div>
