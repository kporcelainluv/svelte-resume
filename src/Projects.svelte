<script>
  export let projects;
  const sprite = "./static/sprite.svg";
  import Icon from "./Icon.svelte";
</script>

<style>
  .link {
    color: #242535;
    font-weight: 500;
    display: inline;
    text-decoration: none;
    font-size: 18px;
  }

  ul {
    margin-top: 8px;
    list-style-type: none;
  }
  li {
    margin-top: 20px;
  }
  p {
    font-size: 16px;
    margin-top: 2px;
    line-height: 22px;
    color: rgba(0, 0, 0, 0.7);
    margin-bottom: 0px;
  }
  .github {
    display: inline-flex;
    align-items: center;
    margin-top: 5px;
    font-size: 14px;
    line-height: 1.5;
    color: rgba(0, 0, 0, 0.7);
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    margin-right: 8px;
  }
  .github:hover {
    text-decoration: none;
    border-bottom: 1px solid #242535;
  }

  .container {
    display: flex;
  }
  .tag {
    font-size: 12px;
    color: rgba(0, 0, 0, 0.7);
  }
</style>

<ul>
  {#each projects as project}
    <li>
      <p class="link">{project.name}</p>
      {#if project.tags}
        <div>
          {#each project.tags as tag}
            <span class="tag">{`sprite.svg#planet`}</span>
          {/each}
        </div>
      {/if}
      <p>
        {@html project.desc}
      </p>

      <div class="container">
        <a target="_blank" class="github" href={project.link}>
          project
          <Icon type="project" />
        </a>

        <a target="_blank" class="github" href={project.github}>
          code
          <Icon type="github" />
        </a>
        {#if project.screenshots}
          <a
            class="github"
            target="_blank"
            href={'https://zhukovairina.now.sh/screens'}>
            screenshots
            <Icon type="screenshots" />
          </a>
        {/if}
      </div>
    </li>
  {/each}
</ul>
