<template>
    <div class="lulu-tooltip" :class="classes"  >
        <slot/>
    </div>
</template>
<script lang="ts">
    import {computed} from 'vue';

    export default {
        props: {
            tooltiptext:{
                type:String,
                default:'text'
            },
        },
        setup(props) {
            const {tooltiptext} = props;
            const classes = computed(() => {
                let tooltiptext;
                return {
                    [`lulu-tooltiptext-${tooltiptext}`]: tooltiptext,
                };
            });
            return {classes};
        }
    };
</script>


<style lang="scss" scoped>
    .lulu-tooltip {
        position: relative;
        display: inline-block;
        .tooltiptext-right {
            visibility: hidden;
            width: 120px;
            background-color: black;
            color: #fff;
            text-align: center;
            border-radius: 6px;
            padding: 5px 0;
            position: absolute;
            z-index: 1;
            top: -5px;
            left: 105%;
        }
        &:hover .tooltiptext-right {
            visibility: visible;
        }
    }

</style>