<div class="slide alt5">
  <h4>Why JWT</h4>

  <div class="diagram scalability">
  {@html scalability}
  </div>
</div>

<ul class="notes">
  <li>JWT is persisted client-side</li>
  <li>JWT is validated server-side</li>
  <li>Use httpOnly flag - client has no access - secure!</li>
  <li>API verifies JWT content using signature on every request - no tinkering</li>
  <li>Persisted client-side as a cookie - browser handles all the passing to + from the API</li>
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