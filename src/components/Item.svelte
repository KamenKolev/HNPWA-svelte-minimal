<script>
  export let index;
  export let url;
  export let title;
  export let domain;
  export let points;
  export let user;
  export let time_ago;
  export let comments_count;
</script>

<style>
  article {
    display: grid;
    grid-template-columns: 3rem auto;
    margin-bottom: 1rem;
    grid-gap: 1rem;
    padding: 0.5rem 1rem;
    box-shadow: 0px 0px 30px 0px rgba(0, 0, 0, 0.1);
  }
  article .left {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5rem;
    font-weight: lighter;
  }
  article h2 {
    margin: 0;
  }
</style>

<article class="itemPreview">
  <div class="left">{index}</div>
  <div class="right">
    <h2>
      <a href={url}>{title}</a>
      {#if domain}
        <small>({domain})</small>
      {/if}
    </h2>
    {#if points}
      <span>{points} points</span>
    {/if}
    {#if user}
      <span>
        by
        <a href={'https://news.ycombinator.com/user?id=' + user}>{user}</a>
      </span>
    {/if}
    {#if time_ago}
      <span>{time_ago}</span>
    {/if}
    {#if comments_count}
      <span>| {comments_count} comments</span>
    {/if}
  </div>
</article>
