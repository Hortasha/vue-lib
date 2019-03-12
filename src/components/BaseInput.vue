<template>
<input
    class='input'
    v-bind:class="{ 'input-error': error === false }"
    v-bind:type="type ? type : 'text'"
    v-bind:placeholder="placeholder ? placeholder : ''"
    v-bind:autoFocus="autoFocus ? true : false"
    v-bind:pattern="reg ? reg : ''"
    v-model="text"
    v-on:keydown="$emit('keydown')"
    v-on:blur="$emit('blur')"
    v-on:input="onInput"
/>
</template>

<script>
export default {
    name: "BaseInput",
    props: {
        type: String,
        autoFocus: Boolean,
        reg: RegExp,
        placeholder: String
    },
    data() {
        return {
            text: "",
            error: false
        }
    },
    beforeMount() {
        this.text = this.$slots.default[0].text;
    },
    methods: {
        onInput() {
            this.error = this.reg.test(this.text);
            console.log(this.error);
        }
    }
}
</script>

<style scoped>
.input {
  display: block;
  margin: 1em 0;
}
.input:focus {
  outline: none;
}

.input-error {
    border: 2px red solid;
}
</style>
