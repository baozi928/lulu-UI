<template>
    <div class="g-container">
        <div class="g-progress"></div>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'Progress'
    }
</script>

<style>
    .g-container {
        width: 240px;
        height: 25px;
        border-radius: 25px;
        background: #eee;
    }
    .g-progress {
        width: 50%;
        height: inherit;
        border-radius: 25px 0 0 25px;
        background: #72bcd5;
    }
</style>