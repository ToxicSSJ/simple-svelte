<script>
 let someVar = `Learning Svelte`;
 let count = 0;
 let styles = { darkMode: false }

 function handleClick() {
    count += 1;
 }

 function toggle() {
   styles.darkMode = !styles.darkMode
   window.document.body.classList.toggle("dark-mode")
 }

</script>

<style>
 p {
   color: var(--theme-color);
 }
 .base-darkMode {
   color: var(--color-light);
 }
 .base-lightMode {
   color: var(--color-dark);
 }
</style>

<div class="About">

  <div class="{!styles.darkMode ? 'base-darkMode' : 'base-lightMode'}">
    {#if !styles.darkMode}
      <p>{someVar}</p>
    {:else}
      <p><span>Hello DarkMode</span></p>
    {/if}
  </div>
  <button on:click={handleClick}>Click {count == 0 ? '' : count}</button>
  <button on:click={toggle}>DarkMode</button>
</div>