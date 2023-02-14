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

<style scoped>
a {
  text-decoration: none;
}
</style>