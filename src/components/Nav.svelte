<script>
  import NavLink from "./NavLink.svelte";
</script>

<style>
  nav ul {
    font-size: 125%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding: 1rem;
    list-style: none;
  }

  nav a {
    color: blue;
  }
  nav a.active {
    color: red;
  }
</style>

<nav>
  <ul>
    <li>
      <NavLink to="/">Top</NavLink>
    </li>
    <li>
      <NavLink to="/newest">Newest</NavLink>
    </li>
    <li>
      <NavLink to="/show">Show</NavLink>
    </li>
    <li>
      <NavLink to="/ask">Ask</NavLink>
    </li>
    <li>
      <NavLink to="/jobs">Jobs</NavLink>
    </li>
  </ul>
</nav>
