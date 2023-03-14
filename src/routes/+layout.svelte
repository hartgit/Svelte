<script>
    import '../main.css';
    import Header from '$lib/+header.svelte';
    import Navigation from '$lib/+nav.svelte';
</script>

<Navigation/>
<Header/>

<section class="slider-container">
    <div> 
        <p class="text">Lorem ipsum dolor sit amet.</p>
    </div>
    <div> 
        <p class="text">Lorem ipsum dolor sit amet.</p>
        
    </div>
    <div> 
        <p class="text">Lorem ipsum dolor sit amet.</p>
    </div>
</section>

<br/>
<slot/>
<br/>



<footer>
    and i am some common footer stuff
</footer>
