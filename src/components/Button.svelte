<script>
  export let count = 0;
  export let value;
</script>

<button on:click>
  {value}
  {count === 0 ? '' : count}
</button>