<!--APIs-->
<script>
  import { onMount } from "svelte";

  let weatherData = [];
 
  function weatherFetch(lat, lng, idx) {
    //Weather API key: d466d663d4fc8c39cad936242a23fc62

    const weatherUrl = "https://api.openweathermap.org";
    const weatherApi = "d466d663d4fc8c39cad936242a23fc62";

    const imgUrl = "https://api.unsplash.com";

    fetch(
      `${weatherUrl}/data/2.5/weather?lat=${lat}&lon=${lng}&units=metric&appid=${weatherApi}`
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
        if (
          weatherData[idx].temperature < 0 &&
          weatherData[idx].weather >= 800
        ) {
          query = "frosty";
        } else if (weatherData[idx].weather == 800) {
          query = "clear+sky";
        } else if (weatherData[idx].weather == 801) {
          query = "light+cloud";
        } else if (weatherData[idx].weather == 802) {
          query = "sky";
        } else if (weatherData[idx].weather == 803) {
          query = "clouds";
        } else if (weatherData[idx].weather == 804) {
          query = "overcast";
        } else if (
          weatherData[idx].weather >= 200 &&
          weatherData[idx].weather < 233
        ) {
          query = "thunderstorm";
        } else if (
          weatherData[idx].weather >= 300 &&
          weatherData[idx].weather < 322
        ) {
          query = "raindrop";
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

        //LocationIQ geocoding API
        const url = "https://us1.locationiq.com";
        const token = "pk.44d2f3c1237317b5d26f968d828e9527";

        fetch(
          `${url}/v1/reverse?key=${token}&lat=${lat}&lon=${lng}&format=json`
        )
          .then((res) => res.json())
          .then((data) => {
            console.log(data);
            weatherData[idx].location = data?.address?.city;
          });

        //image api call
        const clientID = "D82-RRjMGYl6d9Np2EA4QhTgfEU7WX3sLi4Yq5vGwkM";

        fetch(`${imgUrl}/search/photos/?client_id=${clientID}&query=${query}`)
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
    
    setTimeout(() => {
      //London
      weatherFetch("51.5072", "0.1276", 0);
    }, 1000);

    setTimeout(() => {
      //Tokyo
      weatherFetch("35.6762", "139.6503", 1);
    }, 2000);

    setTimeout(() => {
      //Yellowstone
      weatherFetch("44.4157665", "-110.5732942", 2);
    }, 2500);

    setTimeout(() => {
      //Yellowstone
      weatherFetch("44.4157665", "-110.5732942", 2);
    }, 2500);
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
          {item?.location ?? "Loading..."} <br />
          {item?.temperature ?? ""} °C<br />
          {item?.weather ?? ""}<br />
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
    flex-wrap: nowrap;
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
    text-align: center;
    text-shadow: 3px 3px 5px rgb(50, 61, 67);
    padding: 20px;
    font-size: 24px;
    color: white;
    z-index: 2;
    transition: transform 0.5s;
  }

  /* Hover Effects */
  .img-container:hover {
    transform: scale(1.2);
    opacity: 0.7;
    box-shadow: 0 0 50px rgb(104, 104, 104);
  }
  .img-container > .text-overlay:hover {
    transform: scale(1.2);
    opacity: 1;
    text-shadow: 3px 3px 4px rgb(50, 61, 67);
  }


</style>
