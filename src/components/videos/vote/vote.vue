<template>
    <div class="vote">
        <p>Likes: {{ upvotes }}</p>
        <button @click="upvote">Upvote</button>
    </div>
</template>

<script>
    export default {
        name: "upvote",
        data() {
            return {
                upvotes: 0
            }
        },
        methods: {
            upvote() {
                this.upvotes++;
            }
        }
    }
</script>

<style scoped>
    .vote {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }

    p {
        margin-right: 10px;
    }

    button {
        padding: 10px;
        background-color: rebeccapurple;
        color: white;
        border-radius: 5px;
    }
</style>