<script>
  export let skill;
  let fullGroups = Math.floor(skill.years / 5)
  let remainingYears = skill.years % 5
</script>

<style>
  .skill{
    display: flex;
    flex-direction: column; 
    align-items: center; 
    margin-bottom: .5em;
  }

  .skill-name {
    margin-bottom: .5em;
    font-size: 1.5em;
  }

  .bubble{
    width: .7em;
    height: .7em;
    border-radius: 50%;
    background-color: green;
    margin-right: .3em;
  }

  .bubble-stack{
    display: flex;
    margin-bottom: .3em;
  }

  .icons{
    width: 4em;
  }

</style>

<div class="skill">
  <img src={skill.src} class="icons" alt={skill.name}/>
  <div class="skill-name">{skill.name}</div>
  {#each Array(fullGroups) as _}
    <div class="bubble-stack">
      {#each Array(5) as _}
        <span class="bubble"></span>
      {/each}
    </div>
  {/each}
  <div class="bubble-stack">
    {#each Array(remainingYears) as _}
      <span class="bubble"></span>
    {/each}
  </div>
  <span>({skill.years})</span>
</div>
