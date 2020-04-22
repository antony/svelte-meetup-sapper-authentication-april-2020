<div class="slide alt1">
  <h4>The Backend</h4>

  <h5>An API built in HapiJS</h5>

  <ul class="small-fancy-ul">
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

<style>
  .small-fancy-ul {
    padding: 0;
    display: flex;
    text-align: left;
    flex-direction: column;
    align-items: flex-end;
    color: white;
    margin-right: -4.4%;
  }

  .small-fancy-ul li {
    margin: 1vh 0;
    padding: 1vh;
    background-color: #0f0f0f;
    width: 80vw;
    font-size: 2vh;
    margin-left: -4.4%;
  }
</style>