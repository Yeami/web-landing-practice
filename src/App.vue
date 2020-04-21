<template>
    <div id="app" class="container-fluid">
        <header>
            <app-logo-bar
                    :window="window"
                    :items="menuItems"
            />
            <app-nav-bar
                    v-if="window.width >= 768"
                    :items="menuItems"
            />
        </header>
        <main>
            <app-carousel :window="window"/>
            <app-about-us :window="window"/>
        </main>
        <footer>
            <app-footer
                    :window="window"
                    :items="menuItems"
            />
        </footer>
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

        display: flex;
        min-height: 100vh;
        flex-direction: column;
        padding: 0;

        header {
            background-color: white;
        }

        main {
            flex: 1;
            background-color: #F6F7F9;
        }
    }
</style>
