<template>
    <div class="wrapper">
        <div class="logo-block container">
            <div class="left-side"
                 :style="window.width <= 768 ? 'justify-content: center' : ''"
            >
                <img src="@/assets/logo.png" alt="Logo">
                <div class="text">
                    <span class="title">{{title}}</span>
                    <span class="subtitle">{{subtitle}}</span>
                </div>
            </div>
            <div v-if="window.width >= 768"
                 class="right-side"
            >
                <span>{{tagline}}</span>
            </div>
            <div v-if="window.width < 768">
                <img src="@/assets/menu.png"
                     @click="handleMenu()"
                     class="picture"
                     alt="Menu"
                >
            </div>
        </div>
        <div v-if="isMobileMenu"
             class="mobile-menu"
        >
            <span v-for="item in items">
                <a href="#">{{item}}</a>
            </span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppLogoBar',
        props: {
            window: Object,
            items: Array,
        },
        data() {
            return {
                title: 'Пальмира',
                subtitle: 'лучший ресторан',
                tagline: 'Мы рады встретить Вас домашним комфортом!',
                isMobileMenu: false,
            };
        },
        methods: {
            handleMenu() {
                this.isMobileMenu = !this.isMobileMenu;
            }
        }
    }
</script>

<style scoped lang="scss">
    .wrapper {
        .logo-block {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 0.75rem;
            margin-bottom: 0.75rem;
            font-family: 'ArialMT', sans-serif;
            color: #4F4F4F;
            background-color: white;

            .left-side {
                display: flex;
                align-items: center;

                img {
                    width: 2.25rem;
                    height: 2.25rem;
                }

                .text {
                    display: flex;
                    flex-wrap: wrap;
                    max-width: 8rem;
                    line-height: 1;
                    margin-left: 0.5rem;

                    .title {
                        font-size: 1.5rem;
                    }

                    .subtitle {
                        font-size: 0.875rem;
                    }
                }
            }

            .right-side {
                span {
                    font-style: italic;
                }
            }

            .picture {
                height: 2rem;
            }
        }

        .mobile-menu {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            height: 100%;
            background-color: white;

            span {
                font-size: 1.5rem;
                text-transform: uppercase;

                a {
                    text-decoration: none;
                    color: #4F4F4F;
                }
            }
        }
    }
</style>