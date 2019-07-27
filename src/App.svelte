<script>
  import Nav from "./components/Nav.svelte";
  import Page from "./components/Page.svelte";
  export let name;
</script>

<style>
  /* h1 {
    color: purple;
  } */
  /* from react project */
</style>

<div class="App">

  <h1>Hello {name}!</h1>
  <Nav />
  <Page />
</div>
