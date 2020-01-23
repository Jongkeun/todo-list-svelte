<script>
  import H3 from "./components/H3";
  import Article from "./components/Article";
  import MainContainer from "./containers/MainContainer";
  export let name = "like";
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<MainContainer>
  <h1>Hello {name}!</h1>
  <Article {name} />
  <Article {name} />
  <Article {name} />
  <Article {name} />
  <Article {name} />
  <H3 text={name} />
</MainContainer>
