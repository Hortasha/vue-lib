<template>
    <img v-bind:src="url" v-bind:alt="imgAlt ? imgAlt : ''"/>
</template>

<script>
export default {
    name: "BasePicture",
    props: {
        url: String,
        imgAlt: String
    }
}
</script>

<style scoped>

</style>