<script>
    export let jobs;
</script>

<style>
    
    .jobs {
        margin: 0;
    }
    .job {
        margin-bottom: 16px;
    }
     .heading {
        color: #242535;
        font-weight: 500;
        text-decoration: none;
        font-size: 18px;
        display: inline-block;
        margin: 0 0 4px;
    }
    .dates {
        display: flex;
        margin-bottom: 8px;
    }
    
    .date {
        display: inline-flex;
        align-items: center;
        font-size: 14px;
        line-height: 1.5;
    }
    .description-block {
        list-style: none;
        padding-left: 0;
        margin-bottom: 8px;
    }
     .description {
         margin: 0;
         text-decoration: none;
         color: #242535;
         font-size: 16px;
         font-weight: 400;
         line-height: 22px;
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
</style>

<ul class="jobs">
    {#each jobs as job}
        <li class="job">
            <p class="heading">{job.position} at {job.name}</p>
            <div class="dates">
                <span class="date">{job.from} - {job.to}</span>
            </div>
            <ul class="description-block">
                {#each job.description as desc}
                    <li class="description">{desc}</li>
                {/each}
            </ul>
            <ul class="tags">
                {#each job.tags as tag}
                    <li class="tag">{tag}</li>
                {/each}
            </ul>
        </li>
    {/each}
</ul>