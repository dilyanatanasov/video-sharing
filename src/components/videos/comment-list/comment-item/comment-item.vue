<template>
    <div class="comment-item">
        <li>{{from}}: {{message}} {{when}}</li>
    </div>
</template>

<script>
    export default {
        name: "comment-item",
        props: {
            from: String,
            message: String,
            when: String
        }
    }
</script>

<style scoped>
    .comment-item {
        border: 1px solid #eee;
        border-radius: 5px;
        margin: 10px 0;
        padding: 5px;
    }

    li {
        list-style-type: none;
    }
</style>