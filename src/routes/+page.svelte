<!-- CSS Stlying -->

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

<!-- JS -->
<script>
    // const variable does not change
    const num = 42;

    //let variable can be changed
    let first_name = "Lorna";

    let count = 0;

    function incrementCount()
    {
        count++;
    }
</script>

<!-- HTML -->

<div class = "flex-container">
<div><h1>Welcome to SvelteKit {first_name}</h1></div>

</div>



<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<br>
<button on:click={incrementCount}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
</button>