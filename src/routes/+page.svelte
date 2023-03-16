<script>

    import Slider from '$lib/slider.svelte'
</script>

<Slider />

<style> 
.flex-container {
  display: flex;
  background-color: mintcream;
  justify-content: center;
  flex-wrap: wrap;

}

.flex-container > div {
  background-color: #b3e9db;
  margin: 10px;
  padding: 20px;
  font-size: 30px;
}
h1{
    color:rgb(76, 37, 126);
    font-size: 100px;
    font-style: italic;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: normal;
    margin-left: 25%;
    flex-wrap: wrap;
}
button{

    color: darkslateblue;
    font-size: 30px;
    font-family: fantasy;
    background-color: aquamarine;
    padding-right: 5%;
    padding-left: 5%;
    margin-left: 40%;
    flex-wrap: wrap;

}
</style>

