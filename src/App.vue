<template>
  <div id="app">
    <base-section container="container">
      <base-column col="col-12">
        <navbar imgUrl="https://via.placeholder.com/150">
          <nav-item url="#1">Link 1</nav-item>
          <nav-item url="#2">Link 2</nav-item>
          <nav-item url="#3">Link 3</nav-item>
        </navbar>
      </base-column>

      <base-column col="col-6">
        <base-button v-on:clicked="handleClick(10, 5)">
          Click me
        </base-button> 
      </base-column>
      <base-column col="col-6">
        <base-title>Text</base-title>
        <editable-text>Hello World</editable-text> 
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

export default {
  name: 'app',
  components: {
    BaseTitle,
    BaseSection,
    BaseColumn,
    Navbar,
    NavItem,
    BaseButton,
    EditableText
  },
  methods: {
    handleClick(num1, num2) {
      console.log("mordi e mongo " + (num1 + num2));
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