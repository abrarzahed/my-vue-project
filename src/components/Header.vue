<template>
  <div id="nav">
    <div class="logo">
      <router-link to="/"> <h2>Creative agency</h2> </router-link>
    </div>
    <ul :class="{ show: show }" class="menu">
      <li @click="togleMenu" class="first">
        <router-link to="/">Home</router-link>
      </li>
      <li @click="togleMenu">
        <router-link to="/product">Project</router-link>
      </li>
      <li @click="togleMenu">
        <router-link to="/contact">Contact Us</router-link>
      </li>
      <li @click="togleMenu">
        <router-link to="/account">Account</router-link>
      </li>
    </ul>
    <div @click="togleMenu" class="mobile-menu">
      <i v-if="!show" class="fas fa-bars"></i>
      <i v-else class="fas fa-times"></i>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    };
  },
  methods: {
    togleMenu() {
      this.show = !this.show;
    },
  },
};
</script>

<style scoped>
#nav {
  display: flex;
  height: 80px;
  background: #ff9f43;
  align-items: center;
  justify-content: space-between;
}
.logo {
  margin-left: 30px;
}
.logo h2 {
  color: #fff;
  font-size: 28px;
}
.menu {
  display: flex;
  width: auto;
  gap: 20px;
  margin-right: 30px;
}

.menu a {
  padding: 6px 8px;
  border: none;
  color: #fff;
}
.menu a.router-link-exact-active {
  background: #fff;
  color: #ff9f43;
  border-radius: 3px;
}
.mobile-menu {
  position: fixed;
  top: 26px;
  right: 30px;
  color: #333;
  font-size: 30px;
  display: none;
  z-index: 100;
}

@media (max-width: 768px) {
  .mobile-menu {
    display: block;
  }
  .menu {
    display: block;
    position: fixed;
    top: 0;
    right: -30px;
    width: 50%;
    background: #ff9e43c2;
    height: 100%;
    transform: translateX(100%);
    transition: transform 0.3s;
  }
  .menu.show {
    transform: translateX(0);
  }
  li {
    margin: 30px 0 0 40px;
  }
  .first {
    margin-top: 100px;
  }
}

.pop-up {
  width: 80%;
  height: 100vh;
}
</style>
