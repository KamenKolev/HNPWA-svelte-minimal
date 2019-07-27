<script>
  export let apiPath;
  import { onMount } from "svelte";
  import Item from "./Item.svelte";

  apiPath = apiPath || "news";
  let posts = [];
  let page = 1;

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
