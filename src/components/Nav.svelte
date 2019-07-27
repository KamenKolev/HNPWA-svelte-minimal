<script>
  import { Link } from "svelte-routing";
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
      <Link to="/">Top</Link>
    </li>
    <li>
      <Link to="/newest">Newest</Link>
    </li>
    <li>
      <Link to="/show">Show</Link>
    </li>
    <li>
      <Link to="/ask">Ask</Link>
    </li>
    <li>
      <Link to="/jobs">Jobs</Link>
    </li>
  </ul>
</nav>
