<div class="slideshow">
  <svelte:component bind:this={currentSlide} this={$store.slides[$store.index]}></svelte:component>
  <span class="pagination">
    {$store.index + 1} / {$store.slides.length}
  </span>
</div>

<script>
  import key from './key.js'
  import { getContext, onDestroy } from 'svelte'
  const store = getContext(key)

  const bcast = new BroadcastChannel('svelte-present')

  let currentSlide

  bcast.onmessage = function (e) {
    const [ msg, meta ] = e.data.split(':')
    console.log(e.data, msg, meta)
    const directions = {
      next: () => {
        const currentIndex = $store.index
        $store.index = currentIndex >= $store.slides.length - 1 ? currentIndex : currentIndex + 1
      },
      previous: () => {
        const currentIndex = $store.index
        $store.index = currentIndex < 1 ? currentIndex : currentIndex - 1
      },
      key: (meta) => {
        currentSlide.handleKey && currentSlide.handleKey(meta)
      }
    }

    directions[msg] && directions[msg](meta)
  }

  onDestroy(() => {
    bcast.close()
  })
</script>

<style>
  .slideshow {
    overflow: hidden;
  }
</style>