<template>
    <div class="wrapper container-fluid">
        <div :class="window.width >= 1740 ? 'row' : 'container'">
            <div v-if="window.width >= 1740"
                 class="col-md-6"
            >
                <img src="@/assets/about-us.png" alt="About us">
            </div>
            <div :class="window.width >= 1740 ? 'col-md-6' : 'col-md-12'"
                 class="text-wrapper"
            >
                <span class="title">
                    {{title}}
                </span>
                <div class="text">
                    <p v-for="paragraph in paragraphs">
                        {{paragraph}}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppAboutUs',
        props: {
            window: Object,
        },
        data() {
            return {
                title: 'О ресторане',
                paragraphs: [
                    'В ресторане Вас ждет широкий выбор блюд русской, европейской и японской кухни, большой ' +
                    'ассортимент сигар, редких вин, коньяков и других спиртных напитков самого высокого качества.',
                    'Изысканные блюда от шеф-повара приятно удивлят даже самых искушенных гурманов, любителям ' +
                    'восточной экзотики предложат кальян. В ресторане "Пальмира" каждый вечер для гостей звучит ' +
                    'живая музыка. Особый шарм заведению придает веранда на крыше ресторана, откуда открывается ' +
                    'великолепный вид на озеро и лесные холмы.',
                    'В ресторане "Пальмира" можно организовать корпоративные, свадебные вечера, детские праздники и ' +
                    'другие торжества.',
                ],
            };
        },
    }
</script>

<style scoped lang="scss">
    .wrapper {
        padding: 0;

        .row {
            margin: 0;

            .col-md-6 {
                padding: 0;
            }
        }

        .text-wrapper {
            margin-top: 10rem;

            .title {
                font-size: 1.5rem;
                font-weight: bold;
                text-transform: uppercase;
                border: solid 1px black;
                padding: 0.675rem 1.75rem;
            }

            .text {
                max-width: 28rem;
                font-size: 1rem;
                margin-top: 2rem;

                p {
                    margin-bottom: 1.5rem;
                }

                p:last-child {
                    margin-bottom: 0;
                    padding-bottom: 1rem;
                }
            }
        }

        @media screen and (max-width: 1739px) {
            .text-wrapper {
                margin-top: 0;

                .title {
                    border: none;
                    padding: 1rem 0;
                }

                .text {
                    max-width: none;
                    margin: 1rem 0 0;
                }
            }
        }
    }
</style>