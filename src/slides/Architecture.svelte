<div class="slide alt2">
  <h4>Application Architecture</h4>

  <h5>An MVP to demonstrate simple authentication with JWT</h5>
  
  <div class="architecture diagram">
  {@html architecture}
  </div>
</div>

<ul class="notes">
  <li>Based on beyonk.com</li>
  <li>API and Sapper on same domain - cookie seen</li>
  <li>SSR - heavy lifting</li>
  <li>Dumb client</li>
  <li>no seeds or secrets in Sapper</li>
  <li>JWT - cookie is session</li>
  <li>Stateless app</li>
  <li>API handles lifecycle</li>
  <li>JWT Signature verified in backend</li>
  <li>cookie decoded in SSR</li>
  <li>populates session store</li>
  <li>Client uses store</li>
</ul>

<script>
  import architecture from './architecture.svg'
</script>

<style>
  :global(.diagram.architecture svg) {
    width: 40vw;
  }
</style>