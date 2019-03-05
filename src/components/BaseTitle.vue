<template>
  <h1><slot /></h1>
</template>

<script>
export default {
  name: 'BaseTitle',
  props: {
    msg: String
  }
}
</script>

<style scoped>
</style>