<template>
  <div class="product">
    <h2>Few projects</h2>
    <Calculator />
    <Toggle />
    <Gallery />
  </div>
</template>

<script>
import Calculator from "../components/Calculator.vue";
import Toggle from "../components/Toggle.vue";
import Gallery from "../components/Gallery.vue";

export default {
  components: { Calculator, Toggle, Gallery },
};
</script>

<style scoped>
.product {
  padding: 4%;
  background: url(../assets/blo.png);
  background-size: 200%;
  background-repeat: no-repeat;
}
h2 {
  text-align: center;
  margin: 30px 0;
}
h2::first-letter {
  font-size: 40px;
  color: #ff9f43;
}
</style>
