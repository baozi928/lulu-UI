<template>
    <button class="lulu-switch" @click="toggle" :class="{'lulu-checked':value}">
        <span class="pan"></span>
    </button>
</template>
<script lang="ts">
    import {ref} from 'vue';

    export default {
        props: {
            value: Boolean
        },
        setup(props, context) {
            const toggle = () => {
                context.emit('update:value', !props.value); //当前的值取反，通过input事件发送给外界
                //相当于vue2的this.$emit()
            };
            return {toggle};
        }
    };
</script>


<style lang="scss">
    $h: 22px;
    $h2: $h - 4px;
    .lulu-switch {
        height: $h;
        width: $h * 2;
        border: none;
        background: #bfbfbf;
        border-radius: $h/2;
        position: relative;

        > .pan {
            position: absolute;
            top: 2px;
            left: 2px;
            height: $h2;
            width: $h2;
            background: white;
            border-radius: $h2 / 2;
            transition: all 250ms;
        }

        &.lulu-checked {
            background: #1890ff;

            > span {
                left: calc(100% - #{$h2} - 2px);
            }
        }

        &:focus {
            outline: none;
        }

        &:active {
            > span {
                width: $h2 + 4px;
            }
        }

        &.lulu-checked:active {
            > span {
                width: $h2 + 4px;
                margin-left: -4px;
            }
        }
    }
</style>