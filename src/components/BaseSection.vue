<template>
    <section v-bind:class="container">
        <div class="row">
            <slot />
        </div>
    </section>
</template>

<script>
export default {
  name: 'BaseSection',
  props: {
      container: String
  }
}
</script>

<style scoped>
</style>