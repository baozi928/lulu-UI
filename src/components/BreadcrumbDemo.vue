<template>
    <h1>Breadcrumb 示例</h1>
    <Demo :component="Breadcrumb1Demo" />
    <Demo :component="Breadcrumb2Demo"/>
</template>

<script lang="ts">
    import Demo from './Demo.vue'
    import Breadcrumb1Demo from './Breadcrumb1.demo.vue'
    import Breadcrumb2Demo from './Breadcrumb2.demo.vue'
    import {
        ref
    } from 'vue'
    export default {
        components: {
            Demo
        },
        setup() {
            return {
                Breadcrumb1Demo,
                Breadcrumb2Demo
            }
        }
    }
</script>
