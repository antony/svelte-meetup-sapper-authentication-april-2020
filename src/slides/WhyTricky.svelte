<div class="slide alt1">
  <h4>Why is Authentication trickier in Sapper</h4>

  <ul>
    <li>SSR - Server-side / Client-side</li>
    <li>It's authenticating like two separate applications</li>
    <li>It's a mistake to handle authentication in the client-side</li>
  </ul>
</div>

<ul class="notes">
  <li>Two separate applications</li>
  <li>Pick a source of truth (server)</li>
  <li>handle auth at earliest point</li>
  <li>FOC</li>
</ul>
