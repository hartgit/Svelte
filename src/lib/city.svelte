<script>
  let londonText = "london";
  let tokyoText = "tokyoo";
  let pragueText = "praguee";
  let baText = "buenos airess";

  let cities = [
    { name: "London", text: londonText, image: "images/london.jpg" },
    { name: "Tokyo", text: tokyoText, image: "images/tokyo.jpg" },
    { name: "Prague", text: pragueText, image: "images/prague.jpg" },
    { name: "Chicago", text: baText, image: "images/chicago.jpg" },
  ];

  cities = [...cities];
</script>

<div class="city-box">
  {#each cities as city}
    <article class="text">
      <div>
        <h2>{city.name}</h2>
        <p>
          {city.text}
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam nec est quis
          ante euismod faucibus id ut ante. Etiam dictum tellus ut mi consectetur
          accumsan rhoncus ac justo. In nulla justo, auctor at mauris sit amet, aliquet
          elementum tellus. Nulla ac interdum mi. Phasellus egestas mollis nisl at
          mattis. Nulla faucibus ante erat, vel pretium ligula malesuada sit amet.
          Phasellus nec ante est. Duis non turpis vitae lectus tempor placerat sed
          quis risus. Suspendisse quis efficitur nisi, ut pretium lacus. Donec sed
          massa quis diam posuere rhoncus. Class aptent taciti sociosqu ad litora
          torquent per conubia nostra, per inceptos himenaeos. Ut viverra gravida
          sem in efficitur.
        </p>
      </div>
      <div
        class="img-container"
        style="background-image:url({city.image}); background-size: cover"
      />
    </article>
  {/each}
</div>

<style>
  .img-container {
    height: 400px;
    width: 400px;
    margin: 50px;
    border-radius: 30px;
    justify-content: center;
    align-items: center;
  }

  .cities {
    background-color: whitesmoke;
    width: 100%;
    height: 20vh;
    border-radius: 0% 0% 0% 0%;
  }
  .city-box {
    display: flex;
    width: 100%;
    flex-direction: column;
    margin-top: 220px;
  }
  p {
    text-align: justify;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: 1.4rem;
    color: var(--text-color);
    width: 50vw;
    min-width: auto;
  }
  .text {
    display: flex;
    padding-bottom: 50px;
    align-items: center;
    justify-content: center;
  }
</style>
