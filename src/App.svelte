<ShowController />

{#if $store.full}
<Slideshow bind:this={slideshow} />
{:else}
<div class="speaker">
  <div class="deck pane">
    <div class="show-holder">
      <Slideshow bind:this={slideshow} />
    </div>
  </div>
  <div class="note pane">
    <div class="notes-holder">
      <Notes />
    </div>
  </div>
</div>
{/if}

<script>
  import { setContext, onDestroy } from 'svelte'
  import { writable } from 'svelte/store'
  import key from './key.js'
  import slides from './slides/slides.js'

  import ShowController from './ShowController.svelte'
  import Slideshow from './Slideshow.svelte'
  import Notes from './Notes.svelte'

  const store = writable({
    full: true,
    index: 0,
    slides
  })

  setContext(key, store)

  let slideshow

</script>

<style>

  .speaker {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
    height: 100%;
  }

  .pane {
    display: flex;
    flex: 1;
  }

  .deck {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .deck .show-holder {
    width: 90%;
    height: 60%;
  }

  :global(.speaker .pagination) {
    display: none;
  }

  :global(.deck .show-holder .slideshow) {
    zoom: 25%;
  }
</style>