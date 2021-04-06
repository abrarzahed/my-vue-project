<template>
  <div class="home">
    <header>
      <div class="content">
        <h2>the CREATIVE agency</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo atque,
          in esse odio repellat repellendus beatae sapiente omnis eum provident
          a natus! Ipsam iure sapiente nihil velit, doloribus eveniet iusto!
        </p>
        <div class="btn-grp">
          <button>Learn more</button>
          <router-link to="/contact">
            <button class="btn-contact">Contact us</button>
          </router-link>
        </div>
      </div>
    </header>

    <Main />
    <Cta />
  </div>
</template>

<script>
import Main from "../components/Main.vue";
import Cta from "../components/Cta.vue";

export default {
  components: { Main, Cta },
};
</script>
<style scoped>
header {
  display: grid;
  place-items: center;
  min-height: 80vh;
  background: url(../assets/vue1.png);
  background-size: 40%;
  background-repeat: no-repeat;
  background-position: bottom right;
}
.content {
  max-width: 50%;
}
h2 {
  font-size: 32px;
}
p {
  margin: 20px 0;
  line-height: 1.5;
  font-size: 18px;
}
.btn-grp {
  margin-top: 20px;
  display: flex;
  gap: 20px;
}

@media (max-width: 768px) {
  header {
    background-size: 350%;
    background-position: top right;
  }
  .content {
    max-width: 95%;
  }
}
</style>
