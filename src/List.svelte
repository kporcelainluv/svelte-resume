<script>
  export let elements;
</script>

<style>
  a {
    color: rgb(0, 0, 0);
    cursor: pointer;
    font-family: "Helvetica Neue", sans-serif;
    text-decoration: none;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    margin: 0 0 0 8px;
  }
  a:hover {
    color: #92d2f9;
    border-bottom: 1px solid #92d2f9;
  }
  a:focus {
    color: #92d2f9;
    border-bottom: 1px solid #92d2f9;
  }
  ul {
    margin-top: 8px;
  }
  li {
    margin: 0 0 8px 0;
  }
</style>

<ul>
  {#each elements as element}
    <li>
      <a href={element.link}>{element.name}</a>
    </li>
  {/each}
</ul>
