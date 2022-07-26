<script>
    import "../app.css";
    import Navbar from "../components/navbar.svelte";
    import PlatformInfo from "../components/platform/platform-info.svelte";
</script>
<div class="m-0 h-screen w-screen dark:bg-gray-900">
    <div class="container mx-auto xl:w-8/12">
        <Navbar/>
        <PlatformInfo />
    </div>
</div>
<slot />