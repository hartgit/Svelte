<!--Fetch random image for slider-->
<script>
  let img1 ="images/grass.jpg";
  let img2 = "images/sunset.jpg";
  let img3 = "images/deer.jpg";

  const baseurl = "https://api.unsplash.com";

  fetch(`${baseurl}/photos/random/?client_id=D82-RRjMGYl6d9Np2EA4QhTgfEU7WX3sLi4Yq5vGwkM&query=stormy`)
  .then(res => res.json())
  .then(data => {
    console.log(data)
      img1 = data.urls.full;
      console.log(img1);
  })

  fetch(`${baseurl}/photos/random/?client_id=D82-RRjMGYl6d9Np2EA4QhTgfEU7WX3sLi4Yq5vGwkM&query=sunny`)
  .then(res => res.json())
  .then(data => {
    console.log(data)
      img2 = data.urls.full;
      console.log(img2);
  })

</script>

<!--Card Containers-->

<section class="slider-container">
  <section class="cards">
    <div
      class="img-container"
      style="background-image:url({img1}); background-size: cover"
    >
      <div class="text-overlay">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean aliquam
        leo id maximus facilisis.
      </div>
    </div>
    <div
      class="img-container"
      style="background-image:url({img2}); background-size: cover"
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

<!-- CSS -->
<style>
  /* Container Formatting */
  .slider-container {
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: space-between;
  }

  /* Card Formatting */
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

  /* Text Formatting */
  .cards > .img-container > .text-overlay {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    font-size: 24px;
    color: white;
    z-index: 2;
  }

  /* Hover Effects */
  .img-container:hover {
    transform: scale(1.2);
    filter: grayscale();
    opacity: 0.5;
    box-shadow: 0 0 50px rgb(103, 107, 107);
  }

</style>
