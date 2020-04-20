<template>
    <div id="app" class="container-fluid">
        <app-logo-bar/>
        <app-nav-bar/>
    </div>
</template>

<script>
    import AppLogoBar from "./components/LogoBar";
    import AppNavBar from "./components/NavBar";

    export default {
        name: 'App',
        components: {
            AppLogoBar,
            AppNavBar,
        }
    }
</script>

<style lang="scss">
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
</style>
