<template>
  <nav class="desk-nav">
    <div class="navbar">
      <div class="left">
        <ul>
          <li>
            <a href="#"
              ><div
                class="nav-menu"
                @mouseover="showOff(1)"
                @mouseleave="showOn(1)"
              >
                <div class="nav-icon">
                  <img
                    :style="keys == 1 ? off : dispOn"
                    src="../assets/navbar/claim.png"
                    alt=""
                  />
                  <img
                    :style="keys == 1 ? on : dispOff"
                    src="../assets/navbar/claimhv.png"
                    alt=""
                  />
                </div>
                <div :class="keys == 1 ? 'nav-text' : 'nav-text-two'">
                  <p>CLAIM</p>
                </div>
              </div></a
            >
          </li>
          <li>
            <a href="#"
              ><div
                class="nav-menu"
                @mouseover="showOff(2)"
                @mouseleave="showOn(2)"
              >
                <div class="nav-icon">
                  <img
                    :style="keys == 2 ? off : dispOn"
                    src="../assets/navbar/earn.png"
                    alt=""
                  />

                  <img
                    :style="keys == 2 ? on : dispOff"
                    src="../assets/navbar/earnhv.png"
                    alt=""
                  />
                </div>
                <div :class="keys == 2 ? 'nav-text' : 'nav-text-two'">
                  <p>EARN</p>
                </div>
              </div></a
            >
          </li>
          <li>
            <a href="#"
              ><div
                class="nav-menu"
                @mouseover="showOff(3)"
                @mouseleave="showOn(3)"
              >
                <div class="nav-icon">
                  <img
                    :style="keys == 3 ? off : dispOn"
                    src="../assets/navbar/mine.png"
                    alt=""
                  />
                  <img
                    :style="keys == 3 ? on : dispOff"
                    src="../assets/navbar/minehv.png"
                    alt=""
                  />
                </div>
                <div :class="keys == 3 ? 'nav-text' : 'nav-text-two'">
                  <p>MINE</p>
                </div>
              </div></a
            >
          </li>
          <li>
            <a href="#"
              ><div
                class="nav-menu"
                @mouseover="showOff(4)"
                @mouseleave="showOn(4)"
              >
                <div class="nav-icon">
                  <img
                    :style="keys == 4 ? off : dispOn"
                    class="icon-nor"
                    src="../assets/navbar/craft.png"
                    alt=""
                  />
                  <img
                    :style="keys == 4 ? on : dispOff"
                    class="icon-hv"
                    src="../assets/navbar/crafthv.png"
                    alt=""
                  />
                </div>
                <div :class="keys == 4 ? 'nav-text' : 'nav-text-two'">
                  <p>CRAFT</p>
                </div>
              </div></a
            >
          </li>
        </ul>
      </div>
      <div class="middle">
        <img class="w-40" src="../assets/navbar/navlogo.png" alt="" />
      </div>
      <div class="right">
        <ul>
          <li>
            <a href="#"
              ><div
                class="nav-menu"
                @mouseover="showOff(5)"
                @mouseleave="showOn(5)"
              >
                <div class="nav-icon">
                  <img
                    :style="keys == 5 ? off : dispOn"
                    src="../assets/navbar/play.png"
                    alt=""
                  />
                  <img
                    :style="keys == 5 ? on : dispOff"
                    src="../assets/navbar/playhv.png"
                    alt=""
                  />
                </div>
                <div :class="keys == 5 ? 'nav-text' : 'nav-text-two'">
                  <p>PLAY</p>
                </div>
              </div></a
            >
          </li>
          <li>
            <a href="#"
              ><div
                class="nav-menu"
                @mouseover="showOff(6)"
                @mouseleave="showOn(6)"
              >
                <div class="nav-icon">
                  <img
                    :style="keys == 6 ? off : dispOn"
                    src="../assets/navbar/market.png"
                    alt=""
                  />
                  <img
                    :style="keys == 6 ? on : dispOff"
                    src="../assets/navbar/markethv.png"
                    alt=""
                  />
                </div>
                <div :class="keys == 6 ? 'nav-text' : 'nav-text-two'">
                  <p>MARKET</p>
                </div>
              </div></a
            >
          </li>
          <div class="menu-item">
            <div class="header-button">
              <span class="text-3 text-shadow-1">Connect wallet</span>
            </div>
          </div>
        </ul>
      </div>
    </div>
  </nav>

  <NavbarMob class="mobile-nav" />
</template>

<script setup>
import { ref } from "@vue/reactivity";
import { onMounted } from "@vue/runtime-core";
import NavbarMob from "../sub-components/NavbarMob.vue";
const off = ref(null);
const on = ref(null);
const dispOn = ref({ display: "block" });
const dispOff = ref({ display: "none" });
const textShadow = ref();
const col = ref("#1e293b");
let keys = ref();
const showOff = (key) => {
  keys.value = key;
  console.log(keys.value);
  off.value = {
    display: "none",
  };
  on.value = {
    display: "block",
  };
  if (on.value.display == "block") {
    textShadow.value = "1px 2px 20px #f1f5f9";
  }
};
const showOn = (key) => {
  on.value = {
    display: "none",
  };
  off.value = {
    display: "block",
  };
  if (on.value.display == "none") {
    textShadow.value = "";
  }
};

onMounted(() => {
  var meta = document.createElement("meta");
  meta.name = "theme-color";
  document.getElementsByTagName("head")[0].appendChild(meta);
  document
    .querySelector('meta[name="theme-color"]')
    .setAttribute("content", "#291651");
});
</script>

<style lang="scss" scoped>
nav {
  height: 110px;
  padding: 15px;
  // background-color: v-bind(col);
  // background: rgb(15, 23, 42);
  // background: linear-gradient(
  //   180deg,
  //   rgba(15, 23, 42, 1) 0%,
  //   rgba(15, 23, 42, 0.9108018207282913) 89%,
  //   rgba(255, 255, 255, 1) 99%
  // );
  background: rgb(41, 22, 81);
  background: linear-gradient(
    180deg,
    rgba(41, 22, 81, 1) 0%,
    rgba(15, 23, 42, 1) 92%,
    rgba(25, 6, 39, 1) 100%
  );
  background-repeat: no-repeat;
  color: #f1f5f9;
}

.middle {
  font-weight: bold;
  font-size: 35px;
}

.header-button {
  margin-left: 20px;
}

ul li {
  margin-left: 10px;
}

.nav-text {
  font-weight: bold;
  text-shadow: v-bind(textShadow);
}

.nav-text-two {
  font-weight: bold;
}

.menu-item .header-button {
  width: 233px;
  height: 57px;
  background-image: url("../assets/button/buttonbg.png");
  background-size: 100% 100%;
  background-position: center center;
  text-align: center;
  color: rgb(255, 255, 255);
  cursor: pointer;
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: center;
  justify-content: center;
  padding-bottom: 7px;
}

.menu-item .header-button:hover {
  background-image: url("../assets/button/buttonbghover.png");
}

.mobile-nav {
  display: none;
}
@media (max-width: 768px) {
  .desk-nav {
    display: none;
  }
  .mobile-nav {
    display: block;
  }
}
</style>
