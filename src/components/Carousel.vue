<template>
    <div class="wrapper">
        <div class="text-wrapper">
            <div class="text">
                <span class="title">{{title}}</span>
                <span class="subtitle">{{subtitle}}</span>
                <span class="subtitle-time">{{time}}</span>
            </div>
        </div>
        <div v-if="window.width >= 560" class="picture"/>
    </div>
</template>

<script>
    export default {
        name: 'AppCarousel',
        props: {
            window: Object,
        },
        data() {
            return {
                title: 'Бизнес-ланч',
                subtitle: 'в нашем ресторане',
                time: 'с 12.00 до 15.00',
            };
        },
    }
</script>

<style scoped lang="scss">
    .wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #C8CCD2;

        .text-wrapper {
            width: 50%;
            display: flex;
            justify-content: flex-end;
        }

        .text {
            display: flex;
            flex-wrap: wrap;
            font-family: 'ArialMT', sans-serif;
            font-size: 3rem;
            max-width: 30rem;
            line-height: 1;

            .title {
                text-transform: uppercase;
            }

            .title,
            .subtitle-time {
                font-weight: bold;
                color: #71a00c;
            }

            .subtitle {
                color: #464646;
            }
        }

        .picture {
            background: url('../../src/assets/carousel.png') no-repeat;
            background-size: 1218px 600px;
            height: 600px;
            width: 1218px;
        }
    }

    @media screen and (max-width: 1385px) {
        .wrapper {
            .picture {
                background-size: 792px 390px;
                height: 390px;
                width: 792px;
            }
        }
    }

    @media screen and (max-width: 1159px) {
        .wrapper {
            .text-wrapper {
                padding-left: 2rem;

                .text {
                    font-size: 2.5rem;
                }
            }

            .picture {
                background-size: 670px 330px;
                height: 330px;
                width: 670px;
            }
        }
    }

    @media screen and (max-width: 954px) {
        .wrapper {
            .text-wrapper {
                .text {
                    font-size: 2.25rem;
                }
            }

            .picture {
                background-size: 487px 240px;
                height: 240px;
                width: 487px;
            }
        }
    }

    @media screen and (max-width: 559px) {
        .wrapper {
            display: flex;
            justify-content: center;
            align-items: center;

            .text-wrapper {
                width: 100%;
                margin: 0.5rem 0;

                .text {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    text-align: center;
                    max-width: none;
                }
            }
        }
    }

    @media screen and (max-width: 459px) {
        .wrapper {
            .text-wrapper {
                .text {
                    font-size: 2.5rem;
                }
            }
        }
    }
</style>