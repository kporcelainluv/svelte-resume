<script>
  export let courses;
  const headings = Object.keys(courses);
</script>

<style>
  .block-heading {
    padding-left: 0;

    font-weight: 500;
    color: #242535;
    text-decoration: none;
    font-size: 18px;
  }
  .block {
    list-style-type: none;
    padding-left: 0;
    margin-bottom: 0;
  }
  .certificate {
    margin: 0 0 4px;
  }
  .course-heading {
    margin: 0;
    text-decoration: none;
    color: #242535;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    font-size: 16px;
    font-weight: 400;
  }
  .course-heading:hover {
    border-bottom: 1px solid #242535;
  }
  .course-heading:focus {
    border-bottom: 1px solid #242535;
  }

  .additional {
    font-size: 12px;
    font-style: italic;
    color: rgba(0, 0, 0, 0.5);
    line-height: 16px;
  }

  .certificates {
    margin: 0;
  }
</style>

<ul class="certificates">
  {#each headings as heading}
    <li class="block-heading">
      {heading}
      <ul class="block">
        {#each courses[heading] as course}
          <li class="certificate">
            <a class="course-heading" href={course.link}>{course.name}</a>
            <div class="additional">
              <span>{course.company},</span>
              <span>{course.year}</span>
            </div>
          </li>
        {/each}
      </ul>
    </li>
  {/each}
</ul>
