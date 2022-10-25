<template>
    <div class="tooltip">鼠标移动到这里
        <slot></slot>
    </div>
</template>
<script lang="ts">
    import {computed} from 'vue';

    export default {
        props: {
            tooltiptext:{
                type:String,
                default:'tooltiptext'
            },
        },
        setup(props) {
            const {tooltiptext} = props;
            const classes = computed(() => {
                return {
                    [`tooltiptext-${tooltiptext}`]: tooltiptext,
                };
            });
            return {classes};
        }
    };
</script>


<style  scoped>
    .tooltip {
        position: relative;
        display: inline-block;
        padding:0 5px;
    }

</style>