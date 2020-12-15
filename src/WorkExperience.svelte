<script>
    export let jobs;
</script>

<style>
    .block-heading {
        padding-left: 0;
        font-weight: 500;
        color: #242535;
        text-decoration: none;
        font-size: 18px;
        margin-bottom: 16px;
    }

    .additional {
        font-size: 12px;
        font-style: italic;
        color: rgba(0, 0, 0, 0.5);
        line-height: 16px;
    }

    .description {
        font-size: 16px;
        line-height: 22px;
        color: rgba(0, 0, 0, 0.7);
        margin: 0 0 8px;
    }

    .jobs {
        margin: 0;
    }
</style>

<ul class="jobs">
    {#each jobs as job}
        <li class="block-heading">
            {job.position} at {job.name}
            <p class="description">
                {@html job.description}
            </p>
            <div class="additional">
                <span>{job.from} - {job.to}</span>
            </div>
        </li>
    {/each}
</ul>