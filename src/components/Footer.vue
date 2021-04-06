<template>
  <footer>
    <h3>the CREATIVE agency</h3>
    <div class="social-media">
      <i class="fab fa-facebook"></i>
      <i class="fab fa-linkedin"></i>
      <i class="fab fa-instagram"></i>
      <i class="fab fa-youtube"></i>
    </div>
    <div class="subscrive">
      <input type="email" placeholder="Email" />
      <button>Subscrive</button>
    </div>
  </footer>
  <span>Copyright 2020 &copy; developed by Abrar.</span>
</template>

<script>
export default {};
</script>

<style scoped>
footer {
  display: flex;
  min-height: 140px;
  background: #2f2e41;
  align-items: center;
  justify-content: space-between;
  color: #eee;
}
h3 {
  margin-left: 30px;
  font-size: 26px;
}
.social-media {
  display: flex;
  gap: 15px;
  align-items: center;
  font-size: 28px;
  cursor: pointer;
}
.social-media i:hover {
  color: #ff9f43;
}
.subscrive {
  display: flex;
  margin-right: 30px;
  gap: 8px;
}
input {
  padding: 10px;
  border: none;
}
button {
  padding: 10px;
  border: none;
  font-size: 16px;
  font-weight: bold;
  background: #ff9f43;
  color: #fff;
}
span {
  background: #2f2e41;
  text-align: center;
  display: block;
  color: #eee;
  padding: 20px;
}

@media (max-width: 768px) {
  footer {
    flex-wrap: wrap;
    padding: 20px;
    justify-content: center;
    align-items: center;
    gap: 25px;
  }
  h3 {
    margin-left: 0;
  }
  .subscrive {
    margin: 0;
  }
  span {
    margin-top: -5px;
  }
}
</style>
