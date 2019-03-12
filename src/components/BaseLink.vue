<template>
    <a v-bind:href="url">
        <slot />
    </a>
</template>

<script>
export default {
    name: "BaseLink",
    props: {
        url: String
    }
}
</script>

<style scoped>

</style>