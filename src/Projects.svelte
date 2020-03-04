<script>
  export let projects;
</script>

<style>
  .link {
    color: rgb(0, 0, 0);
    cursor: pointer;
    font-family: "Helvetica Neue", sans-serif;
    text-decoration: none;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  }
  .link:hover {
    color: #92d2f9;
    border-bottom: 1px solid #92d2f9;
  }
  .link:focus {
    color: #92d2f9;
    border-bottom: 1px solid #92d2f9;
  }
  ul {
    margin-top: 8px;
  }
  li {
    margin-top: 20px;
  }
  p {
    font-size: 16px;
    margin-top: 2px;
    line-height: 22px;
    color: rgba(0, 0, 0, 0.7);
    margin-bottom: 8px;
  }
  .github {
    display: flex;
    align-items: center;
    margin-top: 5px;
    font-size: 14px;
    border-radius: 25px;
    line-height: 1.5;
    color: rgba(0, 0, 0, 0.7);
  }
  .github:hover {
    color: #92d2f9;
  }
  .github:focus {
    color: #92d2f9;
  }
  svg {
    fill: rgba(0, 0, 0, 0.7);
    padding-left: 5px;
    height: 14px;
    width: 14px;
    padding-bottom: 2px;
  }
  svg:hover {
    fill: #92d2f9;
  }
  .screenshots {
    font-size: 14px;
    color: rgba(0, 0, 0, 0.7);
  }
  .screenshots:hover {
    color: #92d2f9;
  }
</style>

<ul>
  {#each projects as project}
    <li>
      <a target="_blank" class="link" href={project.link}>{project.name}</a>

      <p>{project.desc}</p>

      {#if project.screenshots}
        <a
          class="screenshots"
          target="_blank"
          href={'https://zhukovairina.now.sh/screens'}>
          view screenshots
        </a>
      {/if}
      <a target="_blank" class="github" href={project.github}>
        view on Github
        <svg version="1.1" viewBox="0 0 16 16">
          <path
            fill-rule="evenodd"
            d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47
            7.59.4.07.55-.17.55-.38
            0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01
            1.08.58 1.23.82.72 1.21 1.87.87
            2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95
            0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21
            2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82
            2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87
            3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0
            .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z" />
        </svg>
      </a>

    </li>
  {/each}
</ul>
