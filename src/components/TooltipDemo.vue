<template>
    <div>
        <h1>Tooltip 组件示例 </h1>
        <Demo :component="Tooltip1Demo" />
        <Demo :component="Tooltip2Demo" />
    </div>
</template>

<script lang="ts">
    import Tooltip1Demo from './Tooltip1.demo.vue';
    import Tooltip2Demo from './Tooltip2.demo.vue';
    import Demo from './Demo.vue'

    export default {
        components: {
            Demo
        },
        setup() {
            return {
                Tooltip1Demo,
                Tooltip2Demo,
            };
        }
    };
</script>