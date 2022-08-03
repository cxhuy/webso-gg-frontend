<script>
    import "../app.css";
    import Navbar from "../components/navbar.svelte";
    import Footer from "../components/footer.svelte";
</script>

<div class="m-0 h-min w-min xs:w-screen dark:bg-gray-900">
    <div class="container mx-auto lg:w-10/12 xl:w-8/12">
        <Navbar/>
        <slot />
        <Footer/>
    </div>
</div>

