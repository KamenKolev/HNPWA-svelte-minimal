<script>
  import Nav from "./components/Nav.svelte";
  import Page from "./components/Page.svelte";
  import { Router, Link, Route } from "svelte-routing";
</script>

<style>
  /* h1 {
    color: purple;
  } */
  /* from react project */
</style>

<div class="App">

  <h1>Minimal Svelte HNPWA</h1>
  <Router>
    <Nav />
    <Route component={Page} apiPath="news" lastPage="10" path="/*" />
    <Route component={Page} apiPath="newest" lastPage="12" path="/newest/*" />
    <Route component={Page} apiPath="ask" lastPage="2" path="/ask/*" />
    <Route component={Page} apiPath="show" lastPage="2" path="/show/*" />
    <Route component={Page} apiPath="jobs" lastPage="1" path="/jobs/*" />
  </Router>

  <footer>
    <small>
      Built by
      <a href="https://github.com/KamenKolev/">Kamen Kolev</a>
    </small>
  </footer>
</div>
