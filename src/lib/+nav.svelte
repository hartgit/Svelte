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
    width: 100%;
    position: fixed;
    
  }

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
