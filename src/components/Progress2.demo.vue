<demo>
    环形进度条
</demo>
<template>
 <Progress :size="150" :percent="0.5"/>
</template>

<script>
    import {Progress} from '../lib/index'
    export default {
        components: {Progress},
    }
</script>

