<template>
    <h1>Datepicker 示例</h1>
    <Demo :component="Pagination1Demo" />
<!--    <Demo :component="Pagination2Demo"/>-->
</template>

<script lang="ts">
    import Demo from './Demo.vue'
    import Pagination1Demo from './Pagination1.demo.vue'
    import Pagination2Demo from './Pagination2.demo.vue'
    import {
        ref
    } from 'vue'
    export default {
        components: {
            Demo
        },
        setup() {
            return {
                Pagination1Demo,
                Pagination2Demo
            }
        }
    }
</script>