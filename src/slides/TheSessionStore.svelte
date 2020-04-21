<div class="slide alt1">
  <h4>The session store</h4>

  <ul>
    <li>The session contains profile information as populated in the middleware</li>
    <li>The session is a store and is Reactive</li>
    <li>The JWT might not contain full profile, but it is also your auth token - so just make a request to the API</li>
  </ul>


  <div class="columns">
    <div>
      <pre>
        <span class="component-name">server-side</span>
<span>{serverside.trim()}</span>
      </pre>
    </div>

    <div>
      <pre>
        <span class="component-name">client-side</span>
<span>{clientside.trim()}</span>
      </pre>
    </div>
  </div>
</div>

<script>
const serverside = `<script context="module">
  async function preload (page, session) {
    const { name } = session.profile
    return { name }
  }
<\/script>`

const clientside = `import { stores } from '@sapper/app'
const { session } = stores()

const name = $session.profile.name

<h1>$session.profile.name</h1>`
</script>

<ul class="notes">
  <li>No need to put everything in the profile - JWT is auth</li>
</ul>
