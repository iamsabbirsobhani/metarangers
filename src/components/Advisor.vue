<template>
  <div class="advisors-container">
    <img
      class="advisor-text"
      src="../assets/advisors/img-text-advisor.webp"
      alt=""
    />
    <div class="advisors">
      <div class="advisor" v-for="advisor in advisors" :key="advisor.id">
        <div>
          <img :src="advisor.url" :alt="advisor.alt" />
          <p class="text-1 text-white">{{ advisor.title }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";

const advisors = ref();

advisors.value = [
  {
    id: 0,
    url: new URL("../assets/advisors/mr-harry.webp", import.meta.url).href,
    title: `CEO of Magicave with 28  years exp in the gaming industry , member of Sony's original Playstation launch team and Co-developed the mobile version of Stardew valley.`,
    alt: `Mr. Harry`,
  },
  {
    id: 1,
    url: new URL("../assets/advisors/mr-santiago.webp", import.meta.url).href,
    title: `Crypto-asset investing at ParaFi Capital, Founder of Roca Capital, advisors of Synthetix.`,
    alt: `Mr Santiago`,
  },
  {
    id: 2,
    url: new URL("../assets/advisors/mr-hungdinh.webp", import.meta.url).href,
    title: `Founder of RADA, JoomlArt, DesignBold, VIC Partners.`,
    alt: `Mr Hungdinh`,
  },
];
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.advisors {
  font-family: $pixel-font;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.advisor {
  max-width: 300px;
}
.advisor-text {
  max-width: 50rem;
  margin: 10px auto;
}
@media (max-width: 768px) {
  .advisors {
    flex-direction: column;
  }
  .advisor-text {
    max-width: 22rem;
    margin: 10px auto;
  }
}
</style>
