<script>
  export let projects;
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
  p {
    padding-left: 16px;
    font-size: 16px;
    margin: 6px 0px 12px;
    line-height: 22px;
  }
</style>

<ul>
  {#each projects as project}
    <li>
      <a href={project.link}>{project.name}</a>
      <p>{project.desc}</p>
    </li>
  {/each}
</ul>
