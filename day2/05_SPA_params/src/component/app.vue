<template>
    <div>
        <div class="top"></div>
        <router-view class="body"></router-view>
        <div class="bottom"></div>
    </div>

</template>

<script>
    export default {
        name: "app"
    }
</script>

<style scoped>
    .top{background: #0b2e13;height: 200px;}
    .body{background: skyblue;height: 500px;}
    .bottom{background: blue;height: 200px;}
</style>