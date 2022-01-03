<template>
  <div class="foundation-section">
    <div class="foundation-game">
      <img src="../assets/foundation-game/img-found.webp" alt="found" />
      <div class="foundation-right">
        <img
          src="../assets/foundation-game/img-text-foundation-game.png"
          alt=""
        />
        <p>
          The Paragon Crafting game is the foundation of The Parallel. It is
          where world-building begins. You can gather materials and create any
          Paragon (NFT) you want. Most importantly, your creativity will be
          protected by The Hydra System - an evolving advanced AI copyright
          protection system.
        </p>
      </div>
    </div>
    <div class="about-runes">
      <div class="left">
        <div v-for="ar in aboutRunes" :key="ar.id" class="hrl-item left-items">
          <div class="sc-ezbkAF tltii">
            <img class="ri-img" :src="ar.imgsrc" alt="" /><span
              class="ri-text text-3 text-shadow-1"
              >{{ ar.title }}</span
            >
          </div>
        </div>
      </div>
      <div class="right">
        <img src="../assets/foundation-game/text-about-runes.webp" alt="" />
        <p>
          Runes are the materials that construct The Parallel universe and can
          be found everywhere.
        </p>
        <br />
        <p>
          Runes come in different tiers , as well as different types - greatly
          affecting a crafted paragon power and stats. This gives the foundation
          game several layers of exciting complexity and replayability!.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/runtime-core";
const aboutRunes = ref();

aboutRunes.value = [
  {
    id: 0,
    imgsrc: new URL(`../assets/foundation-game/soil.webp`, import.meta.url)
      .href,
    title: "SOIL",
  },
  {
    id: 1,
    imgsrc: new URL(`../assets/foundation-game/stone.webp`, import.meta.url)
      .href,
    title: "STONE",
  },
  {
    id: 2,
    imgsrc: new URL(`../assets/foundation-game/wood.webp`, import.meta.url)
      .href,
    title: "WOOD",
  },
  {
    id: 3,
    imgsrc: new URL(`../assets/foundation-game/rubber.webp`, import.meta.url)
      .href,
    title: "RUBBER",
  },
  {
    id: 4,
    imgsrc: new URL(`../assets/foundation-game/plastic.webp`, import.meta.url)
      .href,
    title: "PLASTIC",
  },
  {
    id: 5,
    imgsrc: new URL(`../assets/foundation-game/crystal.webp`, import.meta.url)
      .href,
    title: "CRYSTAL",
  },
  {
    id: 6,
    imgsrc: new URL(`../assets/foundation-game/metal.webp`, import.meta.url)
      .href,
    title: "METAL",
  },
  {
    id: 7,
    imgsrc: new URL(`../assets/foundation-game/gem.webp`, import.meta.url).href,
    title: "GEM",
  },
  {
    id: 8,
    imgsrc: new URL(`../assets/foundation-game/onixius.webp`, import.meta.url)
      .href,
    title: "ONIXIUS",
  },
  {
    id: 9,
    imgsrc: new URL(`../assets/foundation-game/crypton.webp`, import.meta.url)
      .href,
    title: "CRYPTON",
  },
  {
    id: 10,
    imgsrc: new URL(`../assets/foundation-game/pythium.webp`, import.meta.url)
      .href,
    title: "PYTHIUM",
  },
  {
    id: 11,
    imgsrc: new URL(`../assets/foundation-game/paranium.webp`, import.meta.url)
      .href,
    title: "PARANIUM",
  },
];
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.foundation-section {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
  width: 1300px;
  margin: auto;
}
.foundation-game {
  display: flex;
  justify-content: space-around;
  align-items: center;
  .foundation-right {
    p {
      color: rgb(255, 255, 255);
      text-align: right;
      font-family: $pixel-font;
      font-size: 18px;
      line-height: 28px;
    }
    img {
      margin-left: auto;
      width: 581px;
      max-width: 90%;
      height: auto;
      margin-bottom: 20px;
    }
  }
}

.about-runes {
  width: 100%;
  display: flex;
  background-image: url("../assets/foundation-game/frame-home-runes.webp");
  background-size: 100% 100%;
  height: 485px;
  padding: 95px 45px 94px 44px;
  margin-bottom: 120px;
  z-index: 0;
  position: relative;
  top: -97px;
}

.left {
  display: flex;
  flex-wrap: wrap;
  flex: 1 1 0%;
  height: 100%;
  align-content: space-between;
}

.right {
  width: 375px;
  margin-bottom: -15px;
  display: flex;
  flex-direction: column;
  -webkit-box-pack: end;
  justify-content: flex-end;
  margin-left: 15px;
  p {
    font-family: $pixel-font;
    color: white;
    font-size: 18px;
  }
}
.left-items {
  width: calc((100% - 60px) / 6);
  margin-right: 12px;
  height: 142px;
  margin: 10px 5px;
}
.tltii {
  display: flex;
  flex-direction: column;
  -webkit-box-align: center;
  align-items: center;
  background-image: url("../assets/foundation-game/foundation-square.png");
  background-size: 100% 100%;
  width: 100%;
  height: 100%;
  padding: 12px 0px 22px;
  span {
    text-align: center;
    text-shadow: 0 2px 0 #3e40e0;
    color: white;
    font-family: $pixel-font;
    letter-spacing: 0.04em;
    font-size: 22px;
    line-height: 20.31px;
  }
}
.tltii .ri-img {
  width: 80px;
  height: 80px;
  margin-bottom: 8px;
}
.cInlsV .home-runes .home-runes-list .hrl-item {
  width: calc((100% - 60px) / 6);
  margin-right: 12px;
  height: 142px;
}

@media (max-width: 768px) {
  .foundation-game {
    flex-direction: column-reverse !important;
    .foundation-right {
      p {
        width: 100%;
        color: rgb(255, 255, 255);
        text-align: left;
        max-width: unset;
        font-family: $pixel-font;
        font-size: 18px;
        line-height: 20px;
        letter-spacing: 0.02em;
        margin: 20px 0;
      }
      img {
        margin: auto;
      }
    }
  }
  .about-runes {
    background-image: url("../assets/foundation-game/frame-home-runes-mobile.webp");
    height: fit-content;
    padding: 24px 21px 30px 20px;
    flex-direction: column-reverse;
    margin-bottom: 50px;
    position: relative;
    top: -41px;
  }
  .tltii {
    span {
      text-align: center;
      text-shadow: 0 2px 0 #3e40e0;
      color: white;
      font-family: $pixel-font;
      letter-spacing: 0.04em;
      font-size: 14px;
      line-height: 20.31px;
    }
  }
  .foundation-game {
    flex-direction: column;
    img {
      max-width: 350px;
    }
  }
  .foundation-section {
    max-width: 350px;
  }
  .left {
    justify-content: center;
  }
  .right {
    margin: 5px auto;
    justify-content: center;
    width: unset;
    img {
      max-width: 300px;
    }
    p {
      max-width: 330px;
      font-size: 14px;
    }
  }

  .left-items {
    width: calc((100% - 60px) / 3);
    margin-right: 12px;
    height: 80px;
    margin: 10px 5px;
  }
  .tltii .ri-img {
    width: 35px;
    height: 80px;
    margin-bottom: 8px;
  }
}
</style>
