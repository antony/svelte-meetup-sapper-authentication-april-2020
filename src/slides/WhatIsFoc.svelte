<div class="slide alt0">
  <h4>Flash of Content</h4>

  <div class="diagram">
    {@html browser}
  </div>
</div>

<ul class="notes">
  <li>this is a FOC</li>
  <li>not rude</li>
  <li>never give a FOC</li>
</ul>

<style>
  .image {
    display: flex;
    justify-content: center;
  }
</style>

<script>
  import { onMount } from 'svelte'
  import browser from './browser.svg'

  let rendered = false

  onMount(() => {
    const interval = setInterval(() => {
      const elem = document.getElementById('tspan948')
      !rendered && (elem.style.display = 'none')
      setTimeout(() => {
        rendered = !rendered
        elem.textContent = rendered ? 'Hello, Svelte' : 'Hello, undefined'
        elem.style.display = 'block'
      }, 100)
    }, 2000)

    return () => clearInterval(interval)
  })
</script>