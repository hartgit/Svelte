

<script>
    import '../main.css';
    import Header from '$lib/+header.svelte';
    import Navigation from '$lib/+nav.svelte';
</script>

<Navigation/>
<Header/>

<br/>
<slot/>
<br/>



<footer>
    and i am some common footer stuff
</footer>
