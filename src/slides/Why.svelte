<div class="slide alt2">
  <h4>Why?</h4>

  <ul class="fancy-ul">
    <li>Authentication is a common requirement</li>
    <li>SSR involves a little more thinking</li>
    <li>A lot of existing solutions only consider the client-side</li>
    <li>Hard to build a generic plug-in</li>
  </ul>
</div>

<ul class="notes">
  <li>Something a lot of apps need</li>
  <li>authenticate the server, source of truth</li>
  <li>tutorials and blogs</li>
  <li>boilerplates, seeds, nice to know how it *works*</li>
</ul>

<style>
  @keyframes slide {
    100% { margin-right: 0 }
  }

  .fancy-ul {
    padding: 0;
    display: flex;
    text-align: right;
    flex-direction: column;
    align-items: flex-end;
    color: white;
    margin-right: -4.4%;
  }

  li {
    margin: 1vh 0;
    padding: 2vh 3%;
    background-color: #0f0f0f;
    width: 70vw;
    font-size: 40px;
    animation: slide 0.5s forwards;
    margin-right: -80vw;
  }

  li:nth-child(1) {
    border-left: 1vw solid #FB0048;
    animation-delay: 1s;
  }

  li:nth-child(2) {
    border-left: 1vw solid #13E708;
    animation-delay: 2s;
  }

  li:nth-child(3) {
    border-left: 1vw solid #4d4dff;
    animation-delay: 3s;
  }

  li:nth-child(4) {
    border-left: 1vw solid #fff;
    animation-delay: 4s;
  }
</style>
