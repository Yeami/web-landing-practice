<template>
    <div id="app" class="container-fluid">
        <app-logo-bar
                :window="window"
                :items="menuItems"
        />
        <app-nav-bar
                v-if="window.width >= 768"
                :items="menuItems"
        />
        <app-carousel :window="window"/>
        <app-about-us :window="window"/>
        <app-footer
                :window="window"
                :items="menuItems"
        />
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
        data() {
            return {
                window: {
                    width: 0,
                    height: 0,
                },
                menuItems: [
                    'Афиша',
                    'Фотоотчеты',
                    'Меню',
                    'Ресторан',
                    'Караоке',
                    'Банкеты',
                    'Контакты',
                ],
            };
        },
        created() {
            window.addEventListener('resize', this.handleResize);
            this.handleResize();
        },
        destroyed() {
            window.removeEventListener('resize', this.handleResize);
        },
        methods: {
            handleResize() {
                this.window.width = window.innerWidth;
                this.window.height = window.innerHeight;
            },
        }
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
