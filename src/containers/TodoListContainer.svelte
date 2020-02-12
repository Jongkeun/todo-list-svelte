<script>
  import { onMount, afterUpdate } from "svelte";
  import Todo from "../components/Todo";
  import Title from "../components/Title";
  import TodoInputBox from "../components/TodoInputBox";
  import { setStorage, getStorage } from "../utils/storage.js";

  let todos = [];

  onMount(() => {
    todos = JSON.parse(getStorage("todos")) || [];
  });

  afterUpdate(() => {
    setStorage("todos", JSON.stringify(todos));
  });

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

  const deleteTodo = id => {
    todos = todos.filter(element => element.id !== id);
  };

  const updateTodo = id => {
    todos = todos.map(element => {
      if (element.id === id) {
        element.isDone = !element.isDone;
      }
      return element;
    });
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
    <Todo {todo} {deleteTodo} {updateTodo} />
  {/each}

</main>
