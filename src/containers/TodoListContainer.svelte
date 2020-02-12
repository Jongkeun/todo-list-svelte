<script>
  import Todo from "../components/Todo";
  import Title from "../components/Title";
  import TodoInputBox from "../components/TodoInputBox";

  let todos = [];

  const generateID = () => {
    return (
      "_" +
      Math.random()
        .toString(36)
        .substr(2, 9)
    );
  };

  const addTodo = content => {
    todos = todos.concat({ id: generateID(), isDone: false, content: content });
  };
</script>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #284b63;
    max-width: 500px;
    margin: auto;
    height: 100%;
  }
</style>

<main>
  <Title />
  <TodoInputBox {addTodo} />
  {#each todos as todo}
    <Todo {todo} />
  {/each}

</main>
