<script>
  import { Tabs, Tab } from 'svelte-chota';
  import DarkMode from './DarkMode.svelte';
  import { GiftIcon, CodeIcon, TerminalIcon } from 'svelte-feather-icons';

  let active_tab = 0;
</script>
<nav class="nav">
  <span class="nav-left">
    <Tabs full bind:active={active_tab}>
      <Tab data-toggle-class= "" 
           data-toggle-target="#tab1"
           data-toggle-radio-group="tabsgroup"
           data-toggle-is-active= "">
           <TerminalIcon size=30 />
           <p>&emsp;</p>
           <GiftIcon size=25 />
           <p>&emsp;</p>
      </Tab>
      <Tab data-toggle-class = ""
           data-toggle-target="#tab2"
           data-toggle-radio-group="tabsgroup"
           class= "">
           <CodeIcon size=30 />
      </Tab>
    </Tabs>
  </span>
  <DarkMode class="nav-right" />
</nav>

