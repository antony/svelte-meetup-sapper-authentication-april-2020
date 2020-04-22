<div class="slide alt1">
  <h4>Why is Authentication trickier in Sapper</h4>

  <div class="diagram">
    {@html states[current]}
  </div>
</div>

<ul class="notes">
  <li>Traditional SPA - Cookie stored in browser - sent to client</li>
  <li>n</li>
  <li>we add SSR into that - no cookie - no session - can't render protected content</li>
  <li>FOC</li>
  <li>solution - browser sends cookie to SSR part - decode contents server-side</li>
  <li>SSR side knows about auth - can call API with JWT - pre-seeds the session</li>
  <li>Cookie can be made httpOnly - cannot be read by clientside - but browser still sends in clientside requests to API</li>
</ul>

<script>
  import ssrOne from './ssr-one.svg'
  import ssrTwo from './ssr-two.svg'
  import ssrThree from './ssr-three.svg'

  const states = [ ssrOne, ssrTwo, ssrThree ]
  let current = 0

  export function handleKey (key) {
    if (key === 'KeyN') {
      current = (current === states.length - 1) ? 0 : ++current
      console.log(current)
    }
  }
</script>

<style>
  .diagram {
    height: 100%;
    align-items: center;
  }
</style>