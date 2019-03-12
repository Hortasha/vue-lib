<template>
    <div v-bind:class="col">
        <slot />
    </div>
</template>

<script>
export default {
  name: 'BaseColumn',
  props: {
      col: String
  }
}
</script>

<style scoped>
</style>