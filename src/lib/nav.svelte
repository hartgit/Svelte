<div class="nav-container">
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="Destinations">Destinations</a></li>
    </ul>
  </nav>

  <div class="nav-transparency" />
</div>

<style>
  /* Navbar Formatting */
  nav {
    display: flex;
    width: 100%;
    justify-content: center;
  }

  nav ul {
    display: flex;
    flex-wrap: wrap;
    list-style: none;
    font-family: "Quicksand", sans-serif;
    font-size:2.5vmax;
    gap: 5rem;
  }

  .nav-container {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    height: 18vmin;
    position: fixed;
  }
  /* Nav Effects */
  .nav-transparency {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgb(216, 216, 216);
    opacity: 0.65;
    filter: blur(9px);
    z-index: -1;
  }
</style>
