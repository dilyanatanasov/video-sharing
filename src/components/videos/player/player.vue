<template>
    <div class="player">
        <iframe :src="video_link" :width="width + '%'" :height="height" title="YouTube video player"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen></iframe>
    </div>
</template>

<script>
    export default {
        name: "Video",
        props: {
            video_link: String,
            width: Number,
            height: Number
        }
    }
</script>

<style scoped>
    .player {
        width: 100%;
        margin: 20px 0;
    }

    iframe {
        border-radius: 5px;
    }
</style>