<template>
    <h1>Steps 示例</h1>
    <Demo :component="Steps1Demo" />
    <Demo :component="Steps2Demo"/>
</template>

<script lang="ts">
    import Demo from './Demo.vue'
    import Steps1Demo from './Steps1.demo.vue'
    import Steps2Demo from './Steps2.demo.vue'
    import {
        ref
    } from 'vue'
    export default {
        components: {
            Demo
        },
        setup() {
            return {
                Steps1Demo,
                Steps2Demo
            }
        }
    }

</script>