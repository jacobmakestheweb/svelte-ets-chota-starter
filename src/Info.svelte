<script>
  import { Col } from 'svelte-chota';
  import { GiftIcon } from 'svelte-feather-icons';

  let src = "https://cdn.glitch.com/9805785a-725c-4d0a-a5cb-788d38e70039%2Fdmcode.png?v=1617671244422" ;
</script>
<style>
:global(.lil-space) {
    padding-top: 6rem;
  }
  .liler-space {
    padding-top: 3.5rem; 
  }
  .bd-primary {
    margin-left:4rem;
    border: 3px solid var(--color-primary)!important;
    border-radius: 20px;
  }
  p {
    font-size: 1.7rem;
  }
</style>
<Col size="6">
    <img {src} alt="dark mode code" height="80%" class="bd-primary" />
</Col>

<Col size="6">
  <h1 class="is-center"> How It Works </h1>
  <p>&emsp;This starter hopes to simplify the scripting of UI components.
    Svelte handles the actual rendering of the components, and the ETS library provides a 
    simple way of switching classes on targeted elements. Combined with Svelte-Chota's easy
    to configure UI kit, this creates a sweet developer experience.
  </p>
  <div class="liler-space"></div>
  <p>&emsp;In the code on the left for the dark mode switch, you can see that we use ETS data
  attributes to switch the theme instead of a js toggle method. This way we can use the 
  button to perform an actual render function, in this case conditionally rendering the 
  icon !
  </p>
  <div class="liler-space"></div>
  <p>&emsp;This lets us write really descriptive markup to describe all of our components
  and save all of our javascript/svelte for stuff like data and rendering.
  <p>
</Col>
  