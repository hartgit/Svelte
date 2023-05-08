<!--APIs-->
<script>
  import { onMount } from "svelte";

  /*let humidity = 0;
  let temperature = 0;
  let weather = 0;*/

  let weatherData = [];

  //let imgs = ["images/grass.jpg", "images/sunset.jpg", "images/deer.jpg"]

  function weatherFetch(lat, lng, idx) {
    //Weather API key: d466d663d4fc8c39cad936242a23fc62

    const weatherUrl = "https://api.openweathermap.org";

    const imgUrl = "https://api.unsplash.com";

    fetch(
      `${weatherUrl}/data/2.5/weather?lat=${lat}&lon=${lng}&units=metric&appid=d466d663d4fc8c39cad936242a23fc62`
    )
      .then((res) => res.json())
      .then((data) => {
        console.log(data);

        //create empty weather array
        weatherData[idx] = {};

        //add items to array
        weatherData[idx].humidity = data?.main?.humidity;
        weatherData[idx].temperature = data?.main?.temp;
        weatherData[idx].weather = data.weather[0].id;

        //if statement sets query to weather condition

        let query;
        if (weatherData[idx].weather == 800) {
          query = "clear-sky";
        } else if (
          weatherData[idx].weather >= 801 &&
          weatherData[idx].weather < 805
        ) {
          query = "clouds";
        } else if (
          weatherData[idx].weather >= 200 &&
          weatherData[idx].weather < 233
        ) {
          query = "thunderstorm";
        } else if (
          weatherData[idx].weather >= 300 &&
          weatherData[idx].weather < 322
        ) {
          query = "drizzle";
        } else if (
          weatherData[idx].weather >= 500 &&
          weatherData[idx].weather < 532
        ) {
          query = "rainy";
        } else if (
          weatherData[idx].weather >= 600 &&
          weatherData[idx].weather < 623
        ) {
          query = "snow";
        } else if (
          weatherData[idx].weather >= 701 &&
          weatherData[idx].weather < 742
        ) {
          query = "fog";
        } else {
          query = "sky";
        }

        const clientID = "D82-RRjMGYl6d9Np2EA4QhTgfEU7WX3sLi4Yq5vGwkM";

        fetch(
          `${imgUrl}/search/photos/?client_id=${clientID}&query=${query}`
        )
          .then((res) => res.json())
          .then((data) => {
            console.log(data);
            weatherData[idx].img = data?.results[0]?.urls?.full;
            weatherData = [...weatherData]; // svelte hack
          });
      });
  }
  //on load calls location and weather data
  onMount(() => {
    //London
    weatherFetch("51.5072", "0.1276", 0);
    //Tokyo
    weatherFetch("35.6762", "139.6503", 1);
    //Barcelona
    weatherFetch("46.3874", "6.1686", 2);
  });
</script>

<!--Card Containers-->

<section class="slider-container">
  <section class="cards">
    {#each weatherData || [] as item}
      <div
        class="img-container"
        style="background-image:url({item?.img ??
          'images/grass.jpg'}); background-size: cover"
      >
        <div class="text-overlay">
          Barcelona <br />
          {item?.temperature ?? "0"} °C<br />
          {item?.humidity ?? "0"}% <br />
          {item?.weather ?? "0"}<br />
        </div>
      </div>
    {/each}
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
