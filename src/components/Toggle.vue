<template>
  <div id="vue-app">
    <h3>Toggle</h3>
    <div class="toggle">
      <div class="btn-wrapper">
        <button class="html" @click="toggleHtml">HTML</button>
        <button class="css" @click="toggleCss">CSS</button>
        <button class="js" @click="toggleJs">JS</button>
      </div>

      <div class="html-block block" v-if="html">
        <h3>This is about HTML</h3>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sunt
          necessitatibus doloremque error mollitia. Totam, molestiae beatae ab
          provident laboriosam enim quasi. Obcaecati eligendi corrupti in. Eos
          sit voluptatem assumenda! Tenetur!
        </p>
      </div>

      <div class="css-block block" v-if="css">
        <h3>This is about CSS</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident
          minima ipsam voluptatibus fuga, ut labore! Adipisci, enim incidunt?
          Est, modi facere. Laboriosam, nam porro in provident ad repellendus.
          Provident, voluptas! Lorem ipsum dolor sit amet consectetur
          adipisicing elit. Quos facere, earum placeat nobis eaque molestiae quo
          a est. Quo optio placeat accusamus deleniti eligendi mollitia nostrum
          dolores harum quibusdam blanditiis!
        </p>
      </div>

      <div class="js-block block" v-if="js">
        <h3>This is about JS</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque
          odio incidunt voluptates, et quam consectetur tenetur enim aspernatur
          eveniet molestias dolores quasi. Modi quis velit nihil doloremque
          dolorem tempora necessitatibus.
        </p>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit.
          Perspiciatis, cumque ad nesciunt doloremque saepe adipisci, placeat
          temporibus illum laudantium modi dolorem consequatur ullam repudiandae
          doloribus facilis odio? Hic, quod explicabo.
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
          quaerat accusantium nam.!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      html: true,
      css: false,
      js: false,
      active: "",
    };
  },
  methods: {
    toggleHtml() {
      {
        this.html = true;
        this.css = false;
        this.js = false;
        this.active = "active-html";
      }
    },
    toggleCss() {
      this.html = false;
      this.css = true;
      this.js = false;
      this.active = "active-css";
    },
    toggleJs() {
      this.html = false;
      this.css = false;
      this.js = true;
      this.active = "active-js";
    },
  },

  computed: {},
};
</script>

<style scoped>
h3 {
  text-align: center;
}
.toggle {
  max-width: 550px;
  margin: 50px auto;
  position: relative;
}
.btn-wrapper {
  position: absolute;
  transform: translateY(-50%);
  display: flex;
  gap: 10px;
}
.html {
  background: #fa8231;
}
.css {
  background: #686de0;
}
.js {
  background: #ee9e40;
}
.btn-wrapper button {
  padding: 10px 20px;
  display: inline-block;
  border: none;
  color: #fff;
}
.btn-wrapper button:focus {
  outline: none;
}
.btn-wrapper button:hover {
  opacity: 0.9;
}
h3 {
  font-family: sans-serif;
  font-size: 20px;
}
.html-block {
  background: #fa8231;
  width: 100%;
}
.css-block {
  background: #686de0;
}
.js-block {
  background: #ee9e40;
}
.block {
  padding: 30px;
  color: #fff;
  border-radius: 10px;
}
.block h3 {
  color: #eee;
  margin: 10px 0;
}
</style>
