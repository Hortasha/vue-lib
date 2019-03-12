<template>
    <nav class="navbarStyle">
        <a href="./">
            <img v-bind:src="imgUrl" alt="icon" />
        </a>
        <ul>
            <slot />
        </ul>
    </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
      imgUrl: String
  }
}
</script>

<style>
.navbarStyle {
  background-color: #EEEEEE;
  width: 100%;
  position: relative;
}
.navbarStyle::after {
  clear: both;
  content: " ";
  display: block;
}
.navbarStyle li {
  display: inline-block;
}
.navbarStyle ul {
  padding: 0;
  margin: 0;
  float: right;
}
.navbarStyle ul a {
  display: block;
  padding: 20px 30px;
  background-color: #D3D3D3;
  text-decoration: none;
  color: #FFFFFF;
}
.navbarStyle ul a:hover {
  background-color: #bababa;
}
.navbarStyle img {
  position: absolute;
  height: 100%;
}
</style>