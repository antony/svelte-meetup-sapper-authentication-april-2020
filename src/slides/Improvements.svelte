<div class="slide alt3">
  <h4>Improvements</h4>

  <ul class="improvements">
    <li>
      <span>@beyonk/sapper-httpclient</span>
      <a href="https://github.com/beyonk-adventures/svelte-mapbox">https://github.com/beyonk-adventures/sapper-httpclient</a>
    </li>
    <li>
      <span>@beyonk/sapper-rbac</span>
      <a href="https://svelte.dev/tutorial/context-api">https://github.com/beyonk-adventures/sapper-rbac</a>
    </li>
  </ul>
</div>

<ul class="notes">
  <li>httpclient wraps fetch/this.fetch</li>
  <li>allows setting default api baseurl</li>
  <li>handles payload decoding from json</li>
  <li>allows graceful handling of errors</li>
  <li>-</li>
  <li>sapper-rbac allows easy guarding of routes</li>
  <li>Allows certain roles to access certain routes using regex</li>
  <li>wraps your middleware with a simple whitelisting interface</li>
</ul>

<style>
  .improvements {
    list-style-type: none;
  }

  .improvements li {
    display: flex;
    align-items: center;
    flex-direction: column;
    margin: 6vh 0;
  }

  .improvements li span {
    font-size: 4vh;
  }
</style>