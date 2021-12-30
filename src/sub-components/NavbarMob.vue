<template>
  <div>
    <nav class="mob-nav mb-4">
      <div>&nbsp;</div>
      <div>
        <img
          class="w-28"
          src="../assets/navbar/navlogo.png"
          alt="Metarangers"
        />
      </div>
      <button v-if="!bool" @click="showMenu">
        <img class="w-8" src="../assets/navbar/navbtnOpen.png" alt="" />
      </button>
      <button v-else @click="showMenu">
        <img class="w-8" src="../assets/navbar/navbtnClose.png" alt="" />
      </button>
    </nav>
    <div
      :style="closeNavMenu"
      :class="bool == true ? 'menu' : 'menu-two'"
      @click="closeMenu"
    >
      <ul
        :class="bool == true ? 'options' : 'turn-back'"
        class="rounded-md m-auto"
      >
        <li>
          <a href="#"
            ><div class="nav-menu">
              <div class="nav-icon">
                <img src="../assets/navbar/claim.png" alt="" />
              </div>
              <div>
                <p>CLAIM</p>
              </div>
            </div></a
          >
        </li>
        <li>
          <a href="#"
            ><div class="nav-menu">
              <div class="nav-icon">
                <img src="../assets/navbar/earn.png" alt="" />
              </div>
              <div>
                <p>EARN</p>
              </div>
            </div></a
          >
        </li>
        <li>
          <a href="#"
            ><div class="nav-menu">
              <div class="nav-icon">
                <img src="../assets/navbar/mine.png" alt="" />
              </div>
              <div>
                <p>MINE</p>
              </div>
            </div></a
          >
        </li>
        <li>
          <a href="#"
            ><div class="nav-menu">
              <div class="nav-icon">
                <img class="icon-nor" src="../assets/navbar/craft.png" alt="" />
              </div>
              <div>
                <p>CRAFT</p>
              </div>
            </div></a
          >
        </li>
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
</template>

<script setup>
import { ref } from "@vue/reactivity";
const col = ref("#1e293b");
const closeNavMenu = ref({ display: "none" });
const bool = ref(false);
const disp = ref();
disp.value = "block";
const closeMenu = (e) => {
  console.log(e.target.classList[0]);
  if (e.target.classList[0] == "menu") {
    setTimeout(() => {
      closeNavMenu.value = {
        display: "none",
      };
      disp.value = "none";
      console.log(disp.value);
    }, 380);
    bool.value = false;
  }
};
const showMenu = (e) => {
  bool.value = !bool.value;
  disp.value = "block";
  console.log(bool.value);
  if (bool.value) {
    closeNavMenu.value = {
      display: "block",
    };
  } else {
    setTimeout(() => {
      closeNavMenu.value = {
        display: "none",
      };
      disp.value = "none";
      console.log(disp.value);
    }, 380);
  }
};
</script>

<style lang="scss" scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 62px;
  padding: 15px;
  background-color: v-bind(col);
  color: #f1f5f9;
  background: rgb(15, 23, 42);
  background: linear-gradient(
    180deg,
    rgba(15, 23, 42, 1) 0%,
    rgba(15, 23, 42, 1) 93%,
    rgba(128, 128, 128, 1) 100%
  );
}
// button {
//   z-index: 10;
//   background-color: #e2e8f0;
//   color: black;
//   border-radius: 4px;
//   width: 100px;
//   height: 40px;
// }

.menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  padding-top: 80px;
  background-color: rgba(128, 128, 128, 0.404);
  z-index: -1;
}

.menu-two {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  padding-top: 80px;
  z-index: -1;
  display: v-bind(disp);
}

.options {
  color: white;
  font-weight: bold;
  text-align: center;
  position: relative;
  display: block;
  height: 540px;
  width: 340px;
  padding: 15px;
  transition: all 0.3s ease-in-out 0s;
  background-image: url("../assets/navbar/navpopup.svg");
  overflow-x: scroll;
  background-size: 100% 103%;
  background-repeat: no-repeat;
  -webkit-animation: automenu-a4541986 0.4s;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  animation: automenu-a4541986 0.4s;
}
.options::-webkit-scrollbar {
  display: block;
}

@keyframes automenu {
  from {
    top: -300px;
    opacity: 0;
  }
  to {
    top: 0;
    opacity: 1;
  }
}
.turn-back {
  color: white;
  font-weight: bold;
  text-align: center;
  position: relative;
  display: block;
  height: 530px;
  width: 340px;
  padding: 15px;
  transition: all 0.3s ease-in-out 0s;
  background-image: url("../assets/navbar/navpopup.svg");
  overflow-x: scroll;
  background-size: 100% 103%;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  animation: turnback 0.4s;
}

li {
  margin: 2px 0;
}
.turn-back::-webkit-scrollbar {
  display: block;
}
@keyframes turnback {
  from {
    top: 0;
    opacity: 1;
  }
  to {
    top: -300px;
    opacity: 0;
  }
}
.sc-efQSVx {
  height: 300px;
}

.idYvEF {
  -webkit-box-align: center;
  align-items: center;
  flex-direction: column;
  position: absolute;
  display: flex;
  right: 0px;
  top: 57px;
  width: 267px;
  height: 0px;
  overflow: hidden;
  transition: all 0.3s ease-in-out 0s;
  padding: 0px 2px 0px 16px;
  background-image: url("../assets/navbar/mobnav.png");
  background-size: 100% 100%;
}

.iincaN {
  -webkit-box-align: center;
  align-items: center;
  flex-direction: column;
  position: absolute;
  display: flex;
  right: 0px;
  top: 57px;
  width: 267px;
  height: 438px;
  overflow: hidden;
  transition: all 0.3s ease-in-out 0s;
  padding: 24px 2px 18px 16px;
  //   background-image: url(data:image/png;base64,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);
  background-image: url("../assets/navbar/mobnav.png");
  background-size: 100% 100%;
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

button {
  float: right;
}
</style>
