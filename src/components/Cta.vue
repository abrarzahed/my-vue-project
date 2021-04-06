<template>
  <div class="cta-container">
    <h4>Contact us for any information</h4>
    <p>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Soluta quis quia
      consequuntur fugit ratione doloribus.
    </p>
    <router-link to="/contact">
      <button class="btn-contact">Contact Us</button></router-link
    >
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.cta-container {
  max-width: 600px;
  margin: 0 auto;
  padding: 40px 2% 80px;
  text-align: center;
}
h4 {
  font-size: 26px;
}
p {
  margin: 15px 0;
}
</style>
