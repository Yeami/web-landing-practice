<template>
    <div class="wrapper">
        <div class="text-wrapper">
            <div class="text">
                <span class="title">Бизнес-ланч</span>
                <span class="subtitle">в нашем ресторане</span>
                <span class="subtitle-time">с 12.00 до 15.00</span>
            </div>
        </div>
        <div class="picture"/>
    </div>
</template>

<script>
    export default {
        name: "AppCarousel",
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
            background: url("../../src/assets/carousel.png") no-repeat;
            background-size: 1218px 600px;
            height: 600px;
            width: 1218px;
        }
    }
</style>