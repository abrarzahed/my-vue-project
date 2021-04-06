<template>
  <div class="main">
    <div class="image">
      <img src="../assets/vue2.png" alt="" />
    </div>
    <div class="content">
      <h4>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatem,
        itaque.
      </h4>
      <p class="middle">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam
        eveniet ad id odit ipsa distinctio molestiae explicabo accusamus nisi,
        asperiores fugit amet atque quae optio quidem veritatis? Commodi, aut
        nulla. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magnam
        maxime hic inventore repellat deleniti quisquam sed ipsum tenetur velit
        ex ipsa
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magnam maxime
        hic inventore repellat deleniti quisquam sed ipsum tenetur velit ex ipsa
        quibusdam nesciunt qui sint sunt, quaerat porro placeat odit.
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.main {
  display: grid;
  grid-template-columns: 1fr 1fr;
  padding: 100px 60px;
  place-items: center;
}
.image img {
  width: 100%;
}
.middle {
  margin: 20px 0;
}
h4 {
  font-size: 22px;
}

@media (max-width: 768px) {
  .main {
    grid-template-columns: 1fr;
    padding: 60px 30px;
  }
}
</style>
