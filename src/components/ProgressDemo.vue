<template>
    <h1>Progress 示例</h1>
    <Demo :component="ProgressDemo" />
</template>

<script lang="ts">
    import Demo from './Demo.vue'
    import ProgressDemo from './Progress.demo.vue'
    import {
        ref
    } from 'vue'
    export default {
        components: {
            Demo
        },
        setup() {
            return {
                ProgressDemo
            }
        }
    }

</script>