<script>
  import Header from "$lib/+header.svelte";
  import City from "$lib/city.svelte";
</script>

<Header headerImg="images/destination.jpg" headerTitle="Destinations" />

<div class="curve-top">
  <div class="title">Cities</div>
  <div class="curve-box" />
</div>

<div class="outer-curve">
  <City />
</div>
<!-- <section class="cities" /> -->

<style>
  .title {
    font-size: 7.6rem;
    color: var(--text-color);
    font-family: "Quicksand", sans-serif;
    display: flex;
    width: 100%;
    position: absolute;
    justify-content: center;
    padding-top: 4.5%;
    padding-left: 35%;
    text-shadow: 2px -2px 3px #222222;
  }

  .curve-top {
    display: flex;
    background-color: var(--curve-color);
    width: 100%;
    height: 30px;
  }
  .curve-box {
    display: flex;
    border-radius: 5% 10% 50% 100%;
    background-color: var(--curve-color);
    height: 180px;
    width: 100%;
  }
  .outer-curve {
    display: flex;
    width: 100%;
    background-color: var(--theme-color);
  }

  .cities {
    background-color: whitesmoke;
    width: 100%;
    height: 20vh;
    border-radius: 0% 0% 0% 0%;
  }
  .city-box {
    display: flex;
    padding: 40px;
    flex-direction: column;
  }
  p {
    text-align: justify;
    font-family:Verdana, Geneva, Tahoma, sans-serif;
    font-size: 1.2rem;
    color: var(--text-color);
  }
</style>
