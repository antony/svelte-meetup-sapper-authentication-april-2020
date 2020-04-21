<div class="slide alt3">
  <h4>The MVP Tech Stack</h4>

  <h5>The Backend (Hapi API)</h5>

  <ul>
    <li>Totally Separate from Sapper</li>
    <li>No need for secrets or sensitive configuration in frontend</li>
    <li>Uses httpOnly cookies for security</li>
    <li>Handles all authentication operations</li>
  </ul>

  <h5>The Frontend (Sapper)</h5>

  <ul>
    <li>"Dumb" - no auth logic</li>
    <li>Uses browser built-ins (fetch) + Sapper's isomorphic "this.fetch"</li>
    <li>The browser does all the work for you</li>
    <li>Server can read the decoded information from JWT</li>
  </ul>

  <h5>JWT</h5>

  <ul>
    <li>Json Web Tokens</li>
    <li>Persisted as a Cookie</li>
    <li>Made up of three parts - a header, payload, and signature</li>
    <li>Server can read the decoded part of the JWT</li>
    <li>API can verify the JWT it recieves using the signature</li>
    <li>Session exists only in the browser - stateless, super-scalable apps</li>
  </ul>
</div>

<ul class="notes">
  <li>Just an overview</li>
  <li>clientside JS - httpOnly flag - no cookie access</li>
</ul>
