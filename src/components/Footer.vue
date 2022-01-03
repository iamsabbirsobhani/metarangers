<template>
  <footer>
    <div class="footer-wrap">
      <img src="../assets/navbar/navlogo.png" alt="" />
      <div
        class="links"
        :class="gridStyle ? `grid grid-cols-2 gap-4` : `grid grid-cols-2 gap-4`"
      >
        <div class="link" v-for="link in links" :key="link.id">
          <a :href="link.url" target="_blank">{{ link.title }}</a>
        </div>
      </div>
      <dir
        class="icons"
        :class="
          gridStyle
            ? `grid grid-cols-4 gap-4`
            : `icons-padding grid grid-cols-8 gap-4`
        "
      >
        <div class="icon" v-for="icon in icons" :key="icon.id">
          <img :src="icon.url" alt="" />
        </div>
      </dir>
    </div>
  </footer>
</template>

<script setup>
import { ref } from "@vue/reactivity";
import { onMounted } from "@vue/runtime-core";
const gridStyle = ref(true);
const links = ref([
  { id: 0, url: "#", title: "PRIVACY POLICY" },
  { id: 1, url: "#", title: "TERMS OF SALE" },
  { id: 2, url: "#", title: "WHITE PAPER" },
  { id: 3, url: "#", title: "EMAIL" },
  { id: 4, url: "#", title: "CONTRACTS" },
  { id: 5, url: "#", title: "PITCH DECK" },
]);

const icons = ref([
  { id: 0, url: new URL("../assets/footer/tiktok.png", import.meta.url).href },
  { id: 1, url: new URL("../assets/footer/twitter.png", import.meta.url).href },
  {
    id: 2,
    url: new URL("../assets/footer/facebook.png", import.meta.url).href,
  },
  { id: 3, url: new URL("../assets/footer/youtube.png", import.meta.url).href },
  { id: 4, url: new URL("../assets/footer/discord.png", import.meta.url).href },
  {
    id: 5,
    url: new URL("../assets/footer/telegram.png", import.meta.url).href,
  },
  { id: 6, url: new URL("../assets/footer/medium.png", import.meta.url).href },
  { id: 7, url: new URL("../assets/footer/reddit.png", import.meta.url).href },
]);

onMounted(() => {
  if (window.innerWidth > 768) {
    gridStyle.value = true;
  } else {
    gridStyle.value = false;
  }
});
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

footer {
  font-family: $pixel-font;
  color: white;
  background-image: url("../assets/footer/bg-footer-2.webp");
  height: 100vh;
  position: relative;
  top: -292px;
  background-repeat: no-repeat;
}

.footer-wrap {
  display: flex;
  position: relative;
  justify-content: space-around;
  align-items: center;
  top: 250px;
}

.links-flex {
  display: flex;
  justify-content: center;
  flex-direction: row;
}

.icons-padding {
  padding: 0;
}
.link {
  a {
    font-size: 22px;
  }
}
@media (max-width: 768px) {
  footer {
    top: -470px;
  }
  .footer-wrap {
    top: 120px;

    flex-direction: column;
    img {
    }
  }
  .link {
    a {
      font-size: 16px;
    }
  }
}
</style>
