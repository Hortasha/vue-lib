<template>
    <button v-on:click="$emit('clicked')" class="button">
        <slot />
    </button>
</template>

<script>
export default {
  name: 'BaseButton'
}
</script>

<style scoped>
.button {
  border: none;
  padding: 7px 20px;
  background-color: #D3D3D3;
  color: #000000;
}

.button:hover {
  background-color: #adadad;
}
</style>