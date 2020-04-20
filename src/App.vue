<template>
    <div id="app" class="container-fluid">
        <app-logo-bar/>
        <app-nav-bar/>
        <app-carousel/>
        <app-about-us/>
        <app-footer/>
    </div>
</template>

<script>
    import AppLogoBar from './components/LogoBar';
    import AppNavBar from './components/NavBar';
    import AppCarousel from './components/Carousel';
    import AppAboutUs from './components/AboutUs';
    import AppFooter from './components/Footer';

    export default {
        name: 'App',
        components: {
            AppFooter,
            AppLogoBar,
            AppNavBar,
            AppCarousel,
            AppAboutUs,
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
