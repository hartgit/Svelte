<section class="slider-container">
  <section class="cards">
    <img src="images/grass.jpg" />
    <img src="images/sunset.jpg" />
    <img src="images/deer.jpg" />
  </section>
</section>

<style>
  .slider-container {
    display: flex;
   
    
    justify-content: center;
    align-items: center;
    align-content: space-between;
   
  }
  
  .cards > img {
    
    background-color: rgb(226, 238, 236);
    border-radius: 30px;
    flex-wrap: wrap;
    width: 250px;
    height: 350px;
    margin: 50px;
    opacity: 1;
    z-index: -2;
  }

  img:hover {
    transform: scale(1.29);
    filter: grayscale();
    opacity: 0.5;
  }
</style>
