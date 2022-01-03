<template>
  <Navbar />
  <FrontPage/>
  <div class="home">
    <SuperAirdrop />
    <TheParallel />
    <FoundationGame />
    <CasualGames />
    <Backers />
    <Advisor />
    <Team />
    <FooterBg />
    <Footer/>
  </div>
</template>

<script setup>
import Navbar from "../components/Navbar.vue";
import SuperAirdrop from "../components/SuperAirdrop.vue";
import TheParallel from "../components/TheParallel.vue";
import FoundationGame from "../components/FoundationGame.vue";
import CasualGames from "../components/CasualGames.vue";
import Backers from "../components/Backers.vue";
import Advisor from "../components/Advisor.vue";
import Team from "../components/Team.vue";
import FooterBg from "../components/FooterBg.vue";
import Footer from "../components/Footer.vue";
import FrontPage from "../components/FrontPage.vue";
</script>

<style lang="scss" scoped>
.home {
  height: 100%;
}
.home::before {
  content: "";
  background-image: url("../assets/super-airdrop/bg-airdrope.png");
  width: 100%;
  height: 1000%;
  background-size: 100%;
  z-index: -2;
  position: absolute;
  top: 1000px;
  left: 0px;
}
.home::after {
  content: "";
  width: 100%;
  height: 100%;
  background-image: url("../assets/super-airdrop/bg-desktop.webp");
  background-repeat: no-repeat;
  background-size: 100% 35%;
  z-index: 0;
  position: absolute;
  top: 872px;
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
    top: 900px;
    left: 0px;
  }
}
</style>
