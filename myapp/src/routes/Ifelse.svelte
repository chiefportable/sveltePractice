<script>
  let x = 12;
  let cats = ["Siamese cat", "British Shorthair", "Persian cat", "Ragdoll"];
  let sportAthletes = [
    {
      name: "Tiger Wood",
      team: "Golf",
    },
    {
      name: "Lionel Messi",
      team: "Football",
    },
    {
      name: "Usain Bolt",
      team: "Running Sport",
    },
  ];
</script>

{#if x > 10}
  <p>{x} is greater than 10</p>
{:else if 5 > x}
  <p>{x} is less than 5</p>
{:else}
  <p>{x} is between 5 and 10</p>
{/if}

<ul>
  {#each sportAthletes as athlete, i}
    <li>
      <span>{athlete.name} {i + 1}</span>
    </li>
  {/each}
</ul>
