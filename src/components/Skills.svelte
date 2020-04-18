<script>
  let skills = [
      {
        id: 1,
        name: 'Java'
      },
      {
        id: 2,
        name: 'C#'
      },
      {
        id: 3,
        name: 'JavaScript'
      },
      {
        id: 4,
        name: 'TypeScript'
      }
  ]
</script>

<style>
  .Skills {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline;
    margin: 0 0 0 0.4em;
  }
</style>

<div class="Skills">
    <h3>Abilities</h3>
    <ul>
      {#each skills as skill, i}
      <li>{skill.name}</li>
      {/each}
    </ul>
</div>