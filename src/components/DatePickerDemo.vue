<template>
    <h1>Datepicker 示例</h1>
    <Demo :component="DatePicker1Demo" />
    <Demo :component="DatePicker2Demo"/>
</template>

<script lang="ts">
    import Demo from './Demo.vue'
    import DatePicker1Demo from './DatePicker1.demo.vue'
    import DatePicker2Demo from './DatePicker2.demo.vue'
    import {
        ref
    } from 'vue'
    export default {
        components: {
            Demo
        },
        setup() {
            return {
                DatePicker1Demo,
                DatePicker2Demo
            }
        }
    }
</script>