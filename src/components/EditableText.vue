<template>

    <div v-if="edit" class="editableText">
        <input
            v-model="text"
            v-on:blur="save"
            v-on:keydown.enter="save"
        />
    </div>

    <div v-else class="editableText">
        <p>
            {{ this.text }}
            <span v-on:click="click">
                <i class="fas fa-pencil-alt"></i>
            </span>
        </p>
    </div>

</template>

<script>
export default {
    name: "EditableText",
    data() {
        return {
            edit: false,
            text: ""
        }
    },
    methods: {
        click() {
            this.edit = true;
        },
        save() {
            this.edit = false;
        }
    },
    beforeMount() {
        this.text = this.$slots.default[0].text;
    }
}
</script>

<style scoped>
.editableText input {
  display: block;
  margin: 1em 0;
}
.editableText p span {
  color: #000000;
  background-color: #90EE90;
  padding: 5px;
  border-radius: 5px;
  cursor: pointer;
}
.editableText p span:hover {
  background-color: #38e038;
}
</style>


