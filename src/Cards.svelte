
<script>
  import { Card, Button, Container} from 'svelte-chota';
 
  // this array holds the data that fills in our card markup
  export const cardData = [
    { id: 1,
      title: 'Svelte', 
      content: 'Svelte is at the core of this starter, which makes rendering UI components simple and very fast',
      docs: 'https://svelte.dev/docs'
    },
    { id: 2, 
      title: 'Chota', 
      content: 'Chota CSS integration with svelte gives us great looking and easy to configure HTML UI components',
      docs:'https://alexxnb.github.io/svelte-chota'
    },
    { id: 3, 
      title: 'Easy-Toggle-State', 
      content: 'Easy-Toggle-State provides HTML attributes for toggling the css class state of any element',
      docs: 'https://twikito.github.io/easy-toggle-state'
    },
  ];
  // the data hash maps to this this object, which we can now loop through in our markup to render recursively
  const cards = {};
</script>
<style>
  .bc {
    margin: 3rem;   
    max-width:300px
  }
</style>
<div class="lil-space"></div>
<Container class="is-center is-full-width">
  {#each cardData as item, i (item.id)}
    <div class="bc" bind:this="{cards[item.id, item.title]}">
        <Card>
            <h4 slot="header">{item.title}</h4>
              {item.content}
            <div slot="footer" class="is-right">
                <Button clear><a href={item.docs}> Docs</a> </Button>
            </div>
        </Card>
    </div>
  {/each}
</Container>
