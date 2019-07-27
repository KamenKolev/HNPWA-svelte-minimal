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
  /* your styles go here */
</style>

<article className="itemPreview">
  <div className="left">{index}</div>
  <div className="right">
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
