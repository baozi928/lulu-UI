<demo>
    普通进度条
</demo>
<template>
    <div class="g-container">
        <div class="g-progress" ></div>
    </div>

</template>

<script lang="ts">
    export default {
        name: 'Progress'
    }
</script>

<style scoped>
    .g-container {
        width: 240px;
        height: 25px;
        border-radius: 25px;
        background: #eeeeee;
        display: flex;
    }
    .g-progress {
        width: 50%;
        height: inherit;
        border-radius: 25px 0 0 25px;
        background: #72bcd5;
    }
</style>