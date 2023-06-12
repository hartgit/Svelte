<script>
  
import { cities } from "../lib/stores";
  

  
</script>

<div class="city-box">
  {#each cities as city}
    <article class="text">
      <div>
        <h2 id={city.name}>{city.name}</h2>
        <p >
          {city.text}
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
