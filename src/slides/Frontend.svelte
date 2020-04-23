<div class="slide alt1">
  <h4>The Frontend</h4>

  <h5>An SSR enabled client built in Sapper</h5>

  <ul class="small-fancy-ul">
    <li>Uses browser built-ins (fetch) + Sapper's isomorphic "this.fetch"</li>
    <li>Requests login session from API and recieves a cookie containing a JWT</li>
    <li>The browser sees the cookie and stores it</li>
    <li>The server-side (SSR) decodes the cookie</li>
    <li>The server-side (SSR) populates the session</li>
    <li>The client-side cannot see the cookie</li>
    <li>The client-side gets all it's information from the session store</li>
  </ul>
</div>

<ul class="notes">
  <li>SSR sees cookie</li>
  <li>SSR pre-seeds session</li>
  <li>Server-side is a source of truth</li>
</ul>

<style>
  .small-fancy-ul {
    padding: 0;
    display: flex;
    text-align: right;
    flex-direction: column;
    align-items: flex-start;
    color: white;
    margin-left: 0;
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