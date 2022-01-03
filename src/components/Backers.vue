<template>
  <div class="backers">
    <img class="text-backers" src="../assets/backers/text-backer.png" alt="" />
    <div
      :class="
        gridStyle
          ? `backers-wrapper-desk grid grid-cols-4 gap-10`
          : `backers-wrapper-mobile grid grid-cols-2 gap-10`
      "
      class="backers-wrapper"
    >
      <div class="backers-logo" v-for="backer in backers" :key="backer.id">
        <img class="backer-img" :src="backer.url" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";
import { onMounted } from "@vue/runtime-core";
// window.innerWidth
const backers = ref();
const gridStyle = ref(true);

backers.value = [
  { id: 0, url: new URL("../assets/backers/keyber.png", import.meta.url).href },
  { id: 1, url: new URL("../assets/backers/signum.png", import.meta.url).href },
  { id: 2, url: new URL("../assets/backers/okex.png", import.meta.url).href },
  {
    id: 3,
    url: new URL("../assets/backers/moonrock.png", import.meta.url).href,
  },
  { id: 4, url: new URL("../assets/backers/rada.png", import.meta.url).href },
  { id: 5, url: new URL("../assets/backers/hub.png", import.meta.url).href },
  { id: 6, url: new URL("../assets/backers/gd10.png", import.meta.url).href },
  { id: 7, url: new URL("../assets/backers/coincu.png", import.meta.url).href },
  { id: 6, url: new URL("../assets/backers/koi.png", import.meta.url).href },
  { id: 7, url: new URL("../assets/backers/ug.png", import.meta.url).href },
  {
    id: 8,
    url: new URL("../assets/backers/redline.png", import.meta.url).href,
  },
  { id: 9, url: new URL("../assets/backers/astrov.png", import.meta.url).href },
];

onMounted(() => {
  if (window.innerWidth > 768) {
    gridStyle.value = true;
  } else {
    gridStyle.value = false;
  }
});
</script>

<style lang="scss" scoped>
.backers-wrapper-desk {
  margin: 50px auto;
}
.backers-logo {
  width: 200px;
  margin: auto;
  display: flex;
}
.backer-img {
  align-self: center;
}
.text-backers {
  width: 35rem;
  margin: auto;
}
@media (max-width: 768px) {
  .backers-wrapper-mobile {
    margin: 50px auto;
  }
  .backers-logo {
    width: 100px;
    margin: auto;
    display: flex;
  }
  .backer-img {
    align-self: center;
  }
  .text-backers {
    width: 20rem;
    margin: auto;
  }
}
</style>
