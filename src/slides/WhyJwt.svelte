<div class="slide alt5">
  <h4>Why JWT</h4>

  <div class="diagram scalability">
  {@html scalability}
  </div>
</div>

<ul class="notes">
  <li>persisted client-side</li>
  <li>validated server-side</li>
  <li>API verifies JWT content using signature on every request - no modification</li>
  <li>browser handles passing to API</li>
  <li>Use httpOnly flag - client has no access - secure!</li>
</ul>

<script>
  import jwt from './jwt.svg'
  import scalability from './scalability.svg'
</script>

<style>
  :global(.diagram.scalability svg) {
    margin-top: 10vh;
    width: 40vw;
  }
</style>