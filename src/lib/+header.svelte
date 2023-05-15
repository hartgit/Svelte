<script>
  export let headerImg = "images/mountains.jpg";
  export let headerTitle = "Weather";
</script>

<section class="header" style="background-image:url({headerImg})">
  <div class="title-overlay">
    <div class="text">{headerTitle}</div>
  </div>
</section>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Koulen&display=swap");
  @import url("https://fonts.googleapis.com/css2?family=Rubik+80s+Fade&family=Rubik+Distressed&display=swap");
  .header {
    background-image: url({headerImg});
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 50vh;
    overflow: hidden;
  }
  .header > .title-overlay {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    font-size: 100px;
    box-sizing: border-box;
    font-family: "Koulen";
    letter-spacing: 0.8rem;
    z-index: 2;
  }
  .title-overlay > .text:hover {
    transition: transform 0.5s;
    transform: scale(1.6);
  }
  .text {
    transition: transform 0.5s;
    background: -webkit-linear-gradient(#e9fafc, #0d6674);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
</style>
