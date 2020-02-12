<script>
  import Todo from "../components/Todo";
  import Title from "../components/Title";
  import TodoInputBox from "../components/TodoInputBox";

  let todos = [
    { id: 1, content: "Hello1" },
    { id: 2, content: "Hello2" },
    { id: 3, content: "Hello3" },
    { id: 4, content: "Hello4" }
  ];
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
  <TodoInputBox />
  {#each todos as todo}
    <Todo {todo} />
  {/each}

</main>
