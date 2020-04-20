<template>
    <div class="container wrapper">
        <div class="left-side">
            <img src="./src/assets/logo.png" alt="Logo">
            <div class="text">
                <span class="title">{{title}}</span>
                <span class="subtitle">{{subtitle}}</span>
            </div>
        </div>
        <div class="right-side">
            <span>{{tagline}}</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppLogoBar',
        data() {
            return {
                title: 'Пальмира',
                subtitle: 'лучший ресторан',
                tagline: 'Мы рады встретить Вас домашним комфортом!',
            };
        },
    }
</script>

<style scoped lang="scss">
    .wrapper {
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
    }
</style>