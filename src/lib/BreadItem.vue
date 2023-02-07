<template>
    <div class="lulu-bread-item">
      <RouterLink v-if="to" :to="to">
        <slot />
      </RouterLink>
      <span v-else>
        <slot />
      </span>
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
        text-decoration:none;
        color: #69aad9;
    }
</style>



