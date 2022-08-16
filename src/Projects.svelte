<script>
  export let projects;
  const sprite = "./static/sprite.svg";
  import Icon from "./Icon.svelte";
</script>

<style>
  .heading {
    color: #242535;
    font-weight: 500;
    text-decoration: none;
    font-size: 18px;
    display: inline-block;
    margin: 0 0 4px;
  }
  .link {
    display: inline-flex;
    align-items: center;
    font-size: 14px;
    line-height: 1.5;
    color: rgba(0, 0, 0, 0.7);
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    margin-right: 16px;
  }
  .link:hover {
    text-decoration: none;
    border-bottom: 1px solid #242535;
  }
  .links {
    display: flex;
    margin-bottom: 8px;
  }
  .tags {
    line-height: 16px;
    font-weight: 500;
    font-style: italic;
    list-style-type: none;
    display: flex;
    flex-wrap: wrap;
    padding-left: 0;
  }
  .tag {
    font-size: 12px;
    color: rgba(0, 0, 0, 0.5);
    margin-right: 8px;
  }
  .description {
    font-size: 16px;
    line-height: 22px;
    color: rgba(0, 0, 0, 0.7);
    margin: 0 0 8px;
  }
  .project {
    margin-bottom: 16px;
  }
  .projects {
    margin-top: 8px;
  }
</style>

<ul class="projects">
  {#each projects as project}
    <li class="project">
      <p class="heading">{project.name}</p>
      <div class="links">
        <a target="_blank" class="link" href={project.link}>
          <Icon type="project" />
          project
        </a>
        {#if project.github}
        <a target="_blank" class="link" href={project.github}>
          <Icon type="github" />
          code
        </a>
        {/if}
        {#if project.screenshots}
          <a
            class="link"
            target="_blank"
            href={'https://zhukovairina.now.sh/screens'}>
            <Icon type="screenshots" />
            screenshots
          </a>
        {/if}
      </div>
      <p class="description">
        {@html project.desc}
      </p>
      {#if project.tags}
        <ul class="tags">
          {#each project.tags as tag}
            <li class="tag">{tag}</li>
          {/each}
        </ul>
      {/if}
    </li>
  {/each}
</ul>
