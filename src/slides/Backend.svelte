<div class="slide alt1">
  <h4>The Backend</h4>

  <h5>An API built in HapiJS</h5>

  <ul>
    <li>Robust hapi-auth-jwt2 plugin</li>
    <li>Default authentication strategy is JWT</li>
    <li>Three routes, create session, retrieve user info, and delete session</li>
    <li>Every time the browser passes the JWT, the authenticity of it's content is validated using the signature</li>
    <li>Invalid cookies / JWTs can be removed with `.unstate()`</li>
  </ul>
</div>

<ul class="notes">
  <li>Secure operations always happen in the API</li>
  <li>If the signature or JWT isn't valid we can delete it</li>
</ul>
