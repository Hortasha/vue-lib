<template>
  <div id="app">
    <base-section container="container">
      <navbar imgUrl="https://via.placeholder.com/150">
        <nav-item url="#1">Link 1</nav-item>
        <nav-item url="#2">Link 2</nav-item>
        <nav-item url="#3">Link 3</nav-item>
      </navbar>
      <base-column col="col-6">
        <base-input v-bind:reg="new RegExp('^[a-z]{3}$', 'i')">Hello</base-input>
        <editable-text>Hello World</editable-text>
        <base-button v-on:clicked="handleClick(10, 5)">
          Click me
        </base-button>
      </base-column>
      <base-column col="col-6">
        <base-link url="//vg.no">Link</base-link>
        <base-para>This is a paragraph</base-para>
        <base-title>Text</base-title>
        <base-picture url="https://cdn.britannica.com/s:300x300/55/174255-004-9A4971E9.jpg" imgAlt="This is a cow" />
      </base-column>
    </base-section>
  </div>
</template>

<script>
import NavItem from './components/NavItem';
import Navbar from './components/Navbar';
import BaseTitle from './components/BaseTitle';
import BaseSection from './components/BaseSection';
import BaseColumn from './components/BaseColumn';
import BaseButton from './components/BaseButton';
import EditableText from './components/EditableText';
import BaseInput from './components/BaseInput';
import BaseLink from './components/BaseLink';
import BasePara from './components/BasePara';
import BasePicture from './components/BasePicture';

export default {
  name: 'app',
  components: {
    BaseTitle,
    BaseSection,
    BaseColumn,
    Navbar,
    NavItem,
    BaseButton,
    EditableText,
    BaseInput,
    BaseLink,
    BasePara,
    BasePicture
  },
  methods: {
    handleClick(num1, num2) {
      console.log(num1 + " " + num2 + " is " + (num1 + num2));
    }
  }
}

</script>

<style>
body {
  margin: 0;
  padding: 0;
  background-color: #FFFFFF;
}
</style>