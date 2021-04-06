<script>
  import { Button } from 'svelte-chota';
  import { SunIcon, MoonIcon } from 'svelte-feather-icons';
  // check it out, no js for switching themes, thanks to easy toggle library
  // this function conditionally renders the correct icon component
  let moon = true;
  let sun = true;
  function iconSwitcher () {
    moon = !moon;
  }
</script>
<style>
    :global(body.dark) {
      --bg-color: #221f22;
      --bg-secondary-color: #131316;
      --font-color: #f5f5f5;
      --color-grey: #ccc;
      --color-darkGrey: #777;
      --color-success: #6df41f;
    }
</style>
<Button clear 
        type="button"
        data-toggle-class-on-target="dark"
        data-toggle-target="body"
        on:click={iconSwitcher}>
        {#if moon}
          <SunIcon size=25 />
        {:else if sun}
          <MoonIcon size=25 />
        {/if}
</Button>
