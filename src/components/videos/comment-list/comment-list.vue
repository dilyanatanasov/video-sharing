<template>
    <div class="comment-list">
        <p>Comments:</p>
        <section class="add-comment">
            <input v-model="newComment" placeholder="Hello..">
            <button @click="addComment">Add</button>
        </section>
        <ul v-for="comment in comments" :key="comment.from">
            <CommentItem :from="comment.from" :message="comment.message" :when="comment.when"></CommentItem>
        </ul>
    </div>
</template>

<script>
    import CommentItem from "./comment-item/comment-item.vue";

    export default {
        name: "comment-list",
        components: {
            CommentItem
        },
        props: {
            comments: [Object]
        },
        data() {
            return {
                newComment: ""
            }
        },
        methods: {
            addComment() {
                this.comments.unshift({
                    from: "me",
                    message: this.newComment,
                    when: "10/10/2021"
                });
                this.newComment = ""
            }
        }
    }
</script>

<style scoped>
    .comment-list {
        width: 95%;
        margin: auto;
    }

    .add-comment {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;
        width: 100%;
    }

    .add-comment input {
        width: 100%;
        height: 100%;
        padding: 9px;
        border: 1px solid #eee;
        border-radius: 5px;
        resize: none;
    }

    .add-comment button {
        padding: 10px 20px;
        background-color: rebeccapurple;
        color: white;
        border-radius: 5px;
    }
</style>