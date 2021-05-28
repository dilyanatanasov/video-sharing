<template>
    <div class="videos">
        <Player :video_link="video_link" :height="height" :width="width"></Player>
        <Vote></Vote>
        <CommentList :comments="comments"></CommentList>
    </div>
</template>

<script>
    import Player from "./player/player.vue";
    import Vote from "./vote/vote";
    import CommentList from "./comment-list/comment-list";

    export default {
        name: "videos",
        components: {
            CommentList,
            Player,
            Vote
        },
        data() {
            return {
                video_link: "https://www.youtube.com/embed/MVpD5AuckSY",
                width: 100,
                height: 300,
                comments: [
                    {
                        from: "Dilyan",
                        message: "hello",
                        when: "12/12/2021"
                    },
                    {
                        from: "Ivan",
                        message: "hello",
                        when: "12/12/2021"
                    },
                    {
                        from: "Marin",
                        message: "hello",
                        when: "12/12/2021"
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    .videos {
        width: 80%;
        margin: 0 10%;
        display: flex;
        flex-direction: column;
    }
</style>