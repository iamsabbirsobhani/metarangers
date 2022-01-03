<template>
  <div class="the-parallel">
    <img
      class="bg-rectangle"
      src="../assets/the-parallel/bg-rectangle-1.png"
      alt=""
    />
    <div class="left">
      <img src="../assets/the-parallel/the-parallel.png" alt="" />
      <p>
        To Kickstart the evolution of an infinite metaverse, where people come
        together to craft a world which cultivates endless social,
        entertainment, gaming and economic opportunities.
      </p>
      <p>Let's immerse into a metaverse where creativity has no limits!</p>
    </div>
    <div class="right">
      <img src="../assets/the-parallel/parallel-cube.webp" alt="" />
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.the-parallel {
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: relative;
  margin: 100px auto;
}
.bg-rectangle {
  position: absolute;
  z-index: -1;
  top: -220px;
}
.left {
  max-width: 600px;
  color: white;
  font-family: $pixel-font;
  font-size: 18px;
  line-height: 28px;
  letter-spacing: 0.02em;
  img {
    margin: 20px 0;
  }
}
.right {
  max-width: 600px;
}

@media (max-width: 768px) {
  .the-parallel {
    flex-direction: column;
  }
  .left {
    max-width: 300px;
    margin: 30px 0;
  }
  .right {
    max-width: 350px;
  }
  .bg-rectangle {
    top: -80px;
  }
}
</style>
