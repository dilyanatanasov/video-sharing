<template>
    <div id="app">
        <Videos></Videos>
    </div>
</template>

<script>
    import Videos from "./components/videos/videos";

    export default {
        name: 'App', 
        components: {
            Videos
        }
    }
</script>

<style>
    * {
        border: 0;
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
    }
</style>
