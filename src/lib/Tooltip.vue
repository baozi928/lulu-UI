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

    .tooltip .tooltiptext-right {
        visibility: hidden;
        width: 120px;
        background-color: rgba(179, 175, 175, 0.99);
        color: #fff;
        text-align: center;
        border-radius: 6px;
        padding: 5px 0;
        position: absolute;
        z-index: 1;
        top: -5px;
        left: 110%;
    }

    .tooltip .tooltiptext-right::after {
        content: "";
        position: absolute;
        top: 50%;
        right: 100%;
        margin-top: -5px;
        border-width: 5px;
        border-style: solid;
        border-color: transparent  rgba(179, 175, 175, 0.99) transparent transparent;
    }
    .tooltip:hover .tooltiptext-right {
        visibility: visible;
    }

</style>