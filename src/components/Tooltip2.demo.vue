<demo>
    常规提示框
</demo>
<template>
    <Tooltip>
        <span class="tooltiptext-right">右边提示文本</span>
    </Tooltip>
    <Tooltip>
        <span class="tooltiptext-left">左边提示文本</span>
    </Tooltip>
    <Tooltip>
        <span class="tooltiptext-up">上方提示文本</span>
    </Tooltip>
    <Tooltip>
        <span class="tooltiptext-down">下方提示文本</span>
    </Tooltip>
</template>

<script>
    import {
        Tooltip
    } from "../lib/index";
    export default {
        components: {
            Tooltip
        }
    }

</script>

<style scoped>
    @import "helper/Tooltip2.css";
</style>
