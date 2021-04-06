
<script>
  import 'chota';
  import { Container } from 'svelte-chota';
  import easyToggle from 'easy-toggle-state';
  import NavBar from './NavBar.svelte';
  import Cards from './Cards.svelte';
  import Info from './Info.svelte';
  
  // dark mode by default if user prefers
  if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
      document.body.classList.add('dark');
  };
  // init easy toggle after DOM loads
  const handler = () => {
    easyToggle();
    document.removeEventListener("DOMContentLoaded", handler);
  };
  document.addEventListener("DOMContentLoaded", handler);
</script>
<style>
  :global(:root) {
    --bg-color: #d8d7d6!important;
    --bg-secondary-color: #f3f3f6;
    --color-primary: #14854F;
    --color-lightGrey: #d2d6dd;
    --color-grey: #747681;
    --color-darkGrey: #3f4144;
    --color-error: #d43939;
    --color-success: #28bd14;
    --grid-maxWidth: 140rem!important;
    --grid-gutter: 0rem;
    --font-size: 1.6rem;
    --font-color: #333333;
    --font-family-sans: sans-serif;
    --font-family-mono: monaco, "Consolas", "Lucida Console", monospace;
  }
</style>
<Container class="is-full-screen">
  <NavBar />
  <div class="lil-space"></div>
  <div id="tab1"class="ui-tabs">
    <Cards />
  </div>
  <div id="tab2"class="ui-tabs">
    <Info />
  </div>
</Container>


