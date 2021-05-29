<template>
    <nav>
        <div>
            <h1>
                Logo
            </h1>
        </div>
        <ul v-for="option in options" :key="option.title">
            <li><a :href="option.link">{{ option.title }}</a></li>
        </ul>
    </nav>
</template>

<script>
    export default {
        name: "navigation",
        data() {
            return {
                options: [
                    {
                        title: "Home",
                        link: "#"
                    },
                    {
                        title: "Videos",
                        link: "#"
                    },
                    {
                        title: "Contact Us",
                        link: "#"
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    nav {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        background-color: rebeccapurple;
        height: 3rem;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
    }

    div {
        margin-right: auto;
    }

    h1 {
        margin: 0 10px;
        color: white;
    }

    li {
        margin: 5px 10px;
        list-style-type: none;
    }

    a {
        text-decoration: none;
        color: white;
    }
</style>