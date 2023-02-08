<Navbar></Navbar>
<slot></slot>
<Footer></Footer>

<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

    :global(*) {
        padding: 0;
        margin: 0;
        font-family: 'Inter', sans-serif;
    }
</style>

<script lang="ts">
    import Navbar from "../components/Navbar.svelte";
    import Footer from "../components/Footer.svelte";
</script>
