<script>
    import "../app.css";
    import Navbar from "../components/navbar.svelte";
</script>

<div class="m-0 h-min w-min xs:w-screen dark:bg-gray-900">
    <div class="container mx-auto xl:w-8/12">
        <Navbar/>
        <slot />
    </div>
</div>

