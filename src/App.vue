<template>
  <Header />
  <router-view />
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
export default {
  components: { Header, Footer },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}
ul {
  list-style: none;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}
button {
  display: inline-block;
  border: 1px solid #ff9f43;
  padding: 15px 25px;
  cursor: pointer;
  font-size: 18px;
  background: transparent;
}
button:focus {
  outline: none;
}
button.btn-contact {
  background: #ff9f43;
  border: 1px solid transparent;
  color: #fff;
}
</style>
