<script>
  export let elements;
</script>

<style>
  a {
    color: black;
    cursor: pointer;
    text-decoration: underline;
  }
  a:hover {
    color: grey;
  }
  a:focus {
    color: grey;
  }
  ul {
    margin-top: 8px;
  }
</style>

<ul>
  {#each elements as element}
    <li>
      <a href={element.link}>{element.name}</a>
    </li>
  {/each}
</ul>
