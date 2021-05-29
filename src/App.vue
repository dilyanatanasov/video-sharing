<template>
    <div id="app">
        <Navigation></Navigation>
        <Videos></Videos>
    </div>
</template>

<script>
    import Videos from "./components/videos/videos";
    import Navigation from "./components/navigation/navigation";

    export default {
        name: 'App', 
        components: {
            Navigation,
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
