<template>
    <div class="wrapper">
        <div class="container">
            <ul>
                <li v-for="item in items">
                    <a href="#">{{item}}</a>
                </li>
            </ul>
            <div class="copywriting">
                <span>{{copywriting}}</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppFooter',
        props: {
            window: Object,
            items: Array,
        },
        data() {
            return {
                copywriting: 'Ⓒ2014 All Rights Reserved.',
            };
        },
    }
</script>

<style scoped lang="scss">
    .wrapper {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        font-family: 'ArialMT', sans-serif;
        background-color: #D1D1D1;

        ul {
            display: flex;
            justify-content: space-between;
            align-items: center;
            list-style: none;
            padding: 0;
            margin: 1rem 0 0;
            line-height: 3rem;

            li {
                flex: 1 1 auto;
                position: relative;
                text-align: center;

                a {
                    text-decoration: none;
                    color: white;
                }
            }
        }

        .copywriting {
            display: flex;
            justify-content: center;
            margin-bottom: 0.5rem;
            color: rgba(44, 44, 44, 0.5);
            font-size: 0.875rem;
        }

        @media screen and (max-width: 559px) {
            ul {
                flex-wrap: wrap;

                li {
                    flex: 0 50%;
                }
            }
        }
    }
</style>