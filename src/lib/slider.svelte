<section class="slider-container">
  <img src = "images/grass.jpg">
  <img src = "images/deer.jpg">
  <img src = "images/sunset.jpg">
</section>

<style>
  .slider-container {
    display: flex;

    height: 400px;
    justify-content: center;
    align-items: center;
    align-content: space-between;
  }
  .slider-container > img {
    background-color: rgb(226, 238, 236);
    border-radius: 30px;
    flex-wrap: wrap;
    width: 250px;
    height: 350px;
    margin: 50px;
    text-align: center;
    font-size: 30px;
    opacity: .65;
  }
</style>
