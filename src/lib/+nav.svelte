<div class="nav-container">
  <nav>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Contact</li>
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
    list-style: none;
    font-family: "Quicksand", sans-serif;
    font-size: 24px;
    
  }

  nav ul li {
    padding: 20px;
    
  }

  .nav-container {
    display: flex;
    width: 100%;
    height: 18vh;
    position: fixed;
    
  }
/* Nav Effects */
  .nav-transparency {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgb(181, 194, 194);
    opacity: 0.5;
    filter: blur(9px);
    z-index: -1;
    
  }
</style>
