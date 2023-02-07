<template>
    <h1>Progress 示例</h1>
    <Demo :component="Progress1Demo" />
    <Demo :component="Progress2Demo"/>
</template>

<script lang="ts">
    import Demo from './Demo.vue'
    import Progress1Demo from './Progress1.demo.vue'
    import Progress2Demo from './Progress2.demo.vue'
    import {
        ref
    } from 'vue'
    export default {
        components: {
            Demo
        },
        setup() {
            return {
                Progress1Demo,
                Progress2Demo
            }
        }
    }

</script>


