<script>
  export let elements;
</script>

<style>
  a {
    text-decoration: none;
    color: #242535;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    margin: 0 0 0 8px;
  }
  a:hover {
    border-bottom: 1px solid #242535;
  }
  a:focus {
    border-bottom: 1px solid #242535;
  }
  ul {
    margin-top: 8px;
  }
  li {
    margin: 0 0 4px 0;
  }
</style>

<ul>
  {#each elements as element}
    <li>
      <a href={element.link}>{element.name}</a>
    </li>
  {/each}
</ul>
