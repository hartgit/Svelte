<section class="slider-container">
  <section class="cards">
    <div
      class="img-container"
      style="background-image:url(images/grass.jpg); background-size: cover"
    >
      <div class="text-overlay">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean aliquam
        leo id maximus facilisis.
      </div>
    </div>
    <div
      class="img-container"
      style="background-image:url(images/sunset.jpg); background-size: cover"
    >
      <div class="text-overlay">hello</div>
    </div>
    <div
      class="img-container"
      style="background-image:url(images/deer.jpg); background-size: cover"
    >
      <div class="text-overlay">hello</div>
    </div>
  </section>
</section>

<style>
  .slider-container {
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: space-between;
  }
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
  }
  .cards > .img-container {
    display: flex;
    height: 350px;
    width: 250px;
    margin: 50px;
    border-radius: 30px;
    justify-content: center;
    align-items: center;
    transition: transform 0.5s;
  }

  .cards > .img-container > .text-overlay {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 25px;
    font-size: 24px;
    color: white;
    z-index: 2;
  }
  .img-container:hover {
    transform: scale(1.2);
    filter: grayscale();
    opacity: 0.5;
    box-shadow: 0 0 50px rgb(103, 107, 107);
  }

  /* old cards
    
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
    transform: scale(1.2);
    filter: grayscale();
    opacity: 0.5;
    box-shadow: 0 0 50px rgb(103, 107, 107);
  }

  .container {
    position: relative;
    text-align: center;
    color: white;
  }
  .container img {
    flex-wrap: wrap;
    object-fit: cover;
    border-radius: 30px;
    margin: 50px;
    width: 250px;
    height: 350px;
    z-index: -2;
  }

  .centered {

    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 1;
  } */
</style>
