<div class="header">
  <div class="title-overlay">Weather</div>
</div>

<style>
 @import url('https://fonts.googleapis.com/css2?family=Rubik+80s+Fade&family=Rubik+Distressed&display=swap');
  .header {
    background-image: url("images/mountains.jpg");
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
    font-family: "Rubik 80s Fade";
    color: rgb(174, 229, 236);
    z-index: 2;
    transition: transform 0.3s;
    
  }
  .header > .title-overlay:hover{
    transform: scale(2);
    
  }
</style>
