<script>
  export let apiPath;
  export let lastPage;
  import { onMount } from "svelte";
  import Item from "./Item.svelte";
  import { Link, Router, navigate } from "svelte-routing";

  let page;
  let posts = [];

  apiPath = apiPath || "news";

  // if the url ends with a number
  page = !isNaN(Number(window.location.pathname.slice(-1)))
    ? Number(window.location.pathname.slice(-1))
    : 1;

  let linkPath =
    apiPath === "news" ? `/${+page + 1}` : `${apiPath}/${+page + 1}`;

  console.log(page);

  onMount(async () => {
    let res = await fetch(`https://api.hnpwa.com/v0/${apiPath}/${page}.json`);
    posts = await res.json();
    // console.log(posts);
  });
</script>

<style>
  ol {
    list-style-type: none;
    margin: none;
    padding: 1rem 0;
  }
</style>

<ol>
  {#each posts as post, index}
    <li>
      <Item index={+index + 1} {...post} />
    </li>
  {/each}
</ol>

<Link to={linkPath}>More</Link>
