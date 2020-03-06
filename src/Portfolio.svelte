<script>
  export let courses;
  const headings = Object.keys(courses);
</script>

<style>
  a {
    text-decoration: none;
    color: #242535;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  }
  a:hover {
    border-bottom: 1px solid #242535;
  }
  a:focus {
    border-bottom: 1px solid #242535;
  }
  .heading {
    padding-left: 40px;
    font-weight: 500;
    color: #242535;
    text-decoration: none;
    font-size: 18px;
    margin: 20px 0 0;
  }
  ul {
    list-style-type: none;
    padding-left: 40px;
    margin: 0 0 30px;
  }
  li {
    font-size: 16px;

    line-height: 22px;
    color: rgba(0, 0, 0, 0.7);
    margin: 10px 0 0;
  }
  .additional {
    font-size: 14px;
    margin-top: 2px;
    line-height: 22px;
    color: rgba(0, 0, 0, 0.7);
  }
  .course-heading {
    margin: 0;
  }
</style>

<div>
  {#each headings as heading}
    <p class="heading">{heading}</p>
    <ul>
      {#each courses[heading] as course}
        <li>
          <p class="course-heading">{course.name}</p>
          <div class="block">
            <span class="additional">{course.company}</span>
            <span class="additional">{course.year}</span>
            <a class="additional" href={course.link}>certificate</a>
          </div>
        </li>
      {/each}
    </ul>
  {/each}
</div>
