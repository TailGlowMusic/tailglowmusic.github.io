<script>
    import logo from '$lib/assets/logo.png';
</script>

<div class="flex flex-col px-10 py-2 w-3/4 mt-10">
    <img src={logo} alt="Tail Glow logo w/ Bird"/>
    
    <div class="flex flex-row justify-around mt-5.5 w-full">
        <a class="h4" href="/music">Music</a>
        <a class="h4" href="/videos">Videos</a>
        <a class="h4" href="/about">About</a>
        <a class="h4" href="/lessons">Lessons</a>
    </div>
</div>

<style>
    img {
        max-height: 63vh;
        margin: 0 auto;
    }
</style>
