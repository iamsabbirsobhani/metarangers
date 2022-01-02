<template>
  <Navbar />
  <div class="home">
    <SuperAirdrop />
    <TheParallel />
    <FoundationGame />
    <CasualGames />
  </div>
</template>

<script setup>
import Navbar from "../components/Navbar.vue";
import SuperAirdrop from "../components/SuperAirdrop.vue";
import TheParallel from "../components/TheParallel.vue";
import FoundationGame from "../components/FoundationGame.vue";
import CasualGames from "../components/CasualGames.vue";
</script>

<style lang="scss" scoped>
.home {
  height: 100%;
}
.home::before {
  content: "";
  background-image: url("../assets/super-airdrop/bg-airdrope.png");
  width: 100%;
  height: 500%;
  background-size: 100%;
  z-index: -2;
  position: absolute;
  top: 340px;
  left: 0px;
}
.home::after {
  content: "";
  width: 100%;
  height: 100%;
  background-image: url("../assets/super-airdrop/bg-desktop.webp");
  background-repeat: no-repeat;
  background-size: 100% 35%;
  z-index: -2;
  position: absolute;
  top: 130px;
  left: 0px;
}

@media (max-width: 768px) {
  .home::before {
    content: "";
    background-image: url("../assets/super-airdrop/bg-airdrope.png");
    width: 100%;
    height: 100%;
    background-size: 100%;
    z-index: -2;
    position: absolute;
    top: 340px;
    left: 0px;
  }
}
</style>
