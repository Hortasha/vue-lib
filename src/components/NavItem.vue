<template>
    <li>
        <a v-bind:href="url">
            <slot />
        </a>
    </li>
</template>

<script>
export default {
  name: 'NavItem',
  props: {
      url: String
  }
}
</script>

<style scoped>
</style>