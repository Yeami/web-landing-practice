<template>
    <div id="app" class="container-fluid">
        <app-logo-bar/>
        <app-nav-bar/>
        <app-carousel/>
    </div>
</template>

<script>
    import AppLogoBar from "./components/LogoBar";
    import AppNavBar from "./components/NavBar";
    import AppCarousel from "./components/Carousel";

    export default {
        name: 'App',
        components: {
            AppLogoBar,
            AppNavBar,
            AppCarousel,
        },
    }
</script>

<style lang="scss">
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        padding: 0;
    }
</style>
