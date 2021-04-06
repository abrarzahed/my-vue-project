<template>
  <h3>Image Gallery</h3>
  <div class="gallery__container">
    <div
      class="gallery"
      :style="{ background: `url(${require(`@/assets/image/${image}`)}` }"
    >
      <!-- <img
        :src="require(`@/assets/image/${image}`)"
        alt=""
        style="border: 1px solid red"
      /> -->

      <h1 class="dummy">Choose Image</h1>
      <!-- {{ background }} -->
    </div>
    <div class="cmn im1" @click="updateGallery(0)">
      <img src="../assets/image/project1.jpg" alt="" />
    </div>
    <div class="cmn im2" @click="updateGallery(1)">
      <img src="../assets/image/project2.jpg" alt="" />
    </div>
    <div class="cmn im3" @click="updateGallery(2)">
      <img src="../assets/image/project3.jpg" alt="" />
    </div>
    <div class="cmn im4" @click="updateGallery(3)">
      <img src="../assets/image/project4.jpg" alt="" />
    </div>
    <div class="cmn im5" @click="updateGallery(4)">
      <img src="../assets/image/project5.jpg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      background: "",
      image: "project1.jpg",
      imageList: [
        "project1.jpg",
        "project2.jpg",
        "project3.jpg",
        "project4.jpg",
        "project5.jpg",
      ],
    };
  },
  methods: {
    updateGallery(pos) {
      this.image = this.imageList[pos];
    },
  },
};
</script>

<style scoped>
.gallery__container {
  max-width: 550px;
  margin: 30px auto;
  background: #ee9e40;
  padding: 20px;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: 4fr 1fr;
  display: grid;
  gap: 20px;
  min-height: 80vh;
  border-radius: 30px;
}
h3 {
  text-align: center;
}
.gallery {
  grid-column: 1 / -1;
  display: grid;
  place-items: center;
  background-size: cover;
  background: url(../assets/image/project3.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  border-radius: 20px;
  transition: background 0.2s linear;
}
img {
  width: 100%;
  border-radius: 10px;
  cursor: pointer;
}
.title {
  text-align: center;
  color: #444;
  font-weight: 200;
  background: #ffffff72;
  width: max-content;
  padding: 10px;
  margin: 0 auto;
  position: absolute;
  top: 200px;
  left: 0;
  transform: rotateZ(-90deg);
  border-radius: 5px;
}
@media (max-width: 768px) {
  .title {
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .gallery__container {
    width: 100%;
    padding: 8px;
    gap: 8px;
    margin: 10px auto;
  }
  .cmn {
    align-self: end;
  }
  .dummy {
    display: none;
  }
}
</style>
