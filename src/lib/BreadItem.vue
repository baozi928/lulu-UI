<template>
    <div class="BreadItem">
        <template v-if="to">
            <router-link :to="to" >
                <slot></slot>
            </router-link>
        </template>
        <template v-else>
            <slot></slot>
        </template>
    </div>
</template>

<script>
    export default {
        props: {
            to: {
                type: [String, Object],
                default: '/',
            },
        },
    }
</script>

<style>
    a:hover{
        text-decoration: none;
        color: #69aad9;
    }
</style>



