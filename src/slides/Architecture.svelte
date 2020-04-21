<div class="slide alt1">
  <h4>Application Architecture</h4>

  <ul>
    <li>Built an MVP</li>
    <li>Based on how Beyonk.com does auth</li>
    <li>
      MVP Overview:
      <ul>
        <li>Stateles Auth - Allows infinite scale</li>
        <li>Auth is stored as a JWT inside a Cookie</li>
        <li>API is responsible for creating and destroying that cookie - the full lifecycle</li>
        <li>JWT Signature is only verified in the backend</li>
        <li>Sapper decodes the cookie data server-side</li>
        <li>Sapper server-side populates session store</li>
        <li>Sapper client simply users what is in the session store</li>
      </ul>
    </li>
  </ul>
</div>

<ul class="notes">
  <li>Sapper server-side (SSR) does heavy lifting</li>
  <li>Sapper client-side is dumb - just shows what it sees</li>
  <li>No JWT seed or secrets in the Sapper app at all</li>
</ul>
