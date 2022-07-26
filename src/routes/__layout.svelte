<script>
    import "../app.css";
    import Navbar from "../components/navbar.svelte";
</script>
<div class="m-0 h-screen w-screen dark:bg-gray-900">
    <div class="container mx-auto lg:w-8/12">
        <Navbar/>
    </div>
</div>
<slot />