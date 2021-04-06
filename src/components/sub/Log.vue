<template>
  <div class="sign">
    <div class="popup" v-if="logedIn">
      <h1>{{ name }} now you are loged in !</h1>
      <router-link to="/">
        <button class="btn-contact">Back to homepage</button></router-link
      >
    </div>

    <form v-else>
      <h2>Log in</h2>
      <input type="text" placeholder="Name" required v-model="name" />
      <input type="password" placeholder="Password" v-model="password" />

      <button @click.prevent="handleSign">Log in</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      password: "",
      logedIn: false,
      loging: true,
    };
  },
  methods: {
    handleSign() {
      if (this.name && this.password === "ad67") {
        this.logedIn = true;
      }
    },
  },
};
</script>

<style scoped>
.sign {
  min-height: 60vh;
  display: grid;
  place-items: center;
  padding: 100px 5% 50px;
}
.popup {
  text-align: center;
}
form {
  width: 40%;
  padding: 30px;
  box-shadow: 0 0 10px rgba(234, 154, 63, 0.693);
  border-radius: 10px;
}
form h2 {
  text-align: center;
}
input {
  display: block;
  width: 80%;
  margin: 20px auto;
  padding: 20px;
}
button {
  width: max-content;
  margin: 10px auto;
  display: block;
}
@media (max-width: 768px) {
  form {
    width: 100%;
    padding: 30px 10px;
  }
  input {
    width: 90%;
  }
}
</style>
