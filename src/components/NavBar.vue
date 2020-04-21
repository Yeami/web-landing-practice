<template>
    <nav class="wrapper">
        <ul class="container">
            <li v-for="item in items">
                <a href="#">{{item}}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
    export default {
        name: 'AppNavBar',
        props: {
            items: Array,
        },
    }
</script>

<style scoped lang="scss">
    .wrapper {
        display: flex;
        justify-content: center;
        font-family: 'ArialMT', sans-serif;
        background-color: #719F0C;
        height: 3rem;

        ul {
            display: flex;
            flex-flow: row wrap;
            justify-content: space-between;
            align-items: center;
            list-style: none;
            padding: 0;
            margin: 0;
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

            li {
                border-left: solid 1px white;
            }

            li:last-child {
                border-right: solid 1px white;
            }
        }
    }
</style>