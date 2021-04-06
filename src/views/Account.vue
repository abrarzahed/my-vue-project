<template>
  <div class="account">
    <!-- <Sign />
  <Log /> -->
    <keep-alive>
      <component :is="component"></component>
    </keep-alive>
    <p v-if="loging">
      Don't have an account?
      <button class="small" @click="togleSign">Sign up</button>
    </p>
    <p v-if="!loging">
      Already have an account?
      <button class="small" @click="togleLog">Log in</button>
    </p>
  </div>
</template>

<script>
import Sign from "../components/sub/Sign.vue";
import Log from "../components/sub/Log.vue";
export default {
  components: { Sign, Log },
  data() {
    return {
      component: "Log",
      loging: true,
    };
  },
  methods: {
    togleSign() {
      this.component = "Sign";
      this.loging = !this.loging;
    },
    togleLog() {
      this.component = "Log";
      this.loging = !this.loging;
    },
  },
};
</script>

<style scoped>
.account {
  background: url(../assets/blo2.png);
  background-size: cover;
  background-repeat: no-repeat;
}
.small {
  padding: 5px;
  border: none;
  text-decoration: underline;
}
p {
  text-align: center;
  margin: 30px;
}
</style>
