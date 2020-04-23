<div class="slide alt5">
  <h4>What is a JWT</h4>

  <div class="diagram">
  {@html jwt}
  </div>
</div>

<ul class="notes">
  <li>auth token</li>
  <li>comprised of three parts - header, payload, signature</li>
  <li>Readable, editable client-side, no secret keys needed - signature validates integrity</li>
  <li>JWT is your session</li>
</ul>

<script>
  import jwt from './jwt.svg'
  import scalability from './scalability.svg'
</script>