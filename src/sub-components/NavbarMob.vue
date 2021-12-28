<template>
  <div>
    <nav class="mob-nav mb-4">
      <button @click="showMenu">Button</button>
    </nav>
    <div
      :class="bool == true ? 'menu' : 'menu-two'"
      @click="closeMenu"

    >
      <ul
        :class="bool == true ? 'options' : 'turn-back'"
        class="w-96 rounded-md p-4 bg-blue-600 h-28 m-auto"
      >
        <li>Lorem</li>
        <li>Ipsum</li>
        <li>Dolor</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";
const col = ref("#1e293b");
const closeNavMenu = ref({ display: "none" });
const bool = ref(false);

const closeMenu = (e) => {
  console.log(e.target.classList[0]);
  if (e.target.classList[0] == "menu") {
    closeNavMenu.value = {
      display: "none",
    };
    bool.value = false;
  }
};
const showMenu = (e) => {
  bool.value = !bool.value;
  console.log(bool.value);
  if (bool.value) {
    closeNavMenu.value = {
      display: "block",
    };
  } else {
    closeNavMenu.value = {
      display: "none",
    };
  }
};
</script>

<style lang="scss" scoped>
nav {
  height: 100px;
  padding: 15px;
  background-color: v-bind(col);
  color: #f1f5f9;
}
button {
  z-index: 10;
  background-color: #e2e8f0;
  color: black;
  border-radius: 4px;
  width: 100px;
  height: 40px;
}

.menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  padding-top: 200px;
  background-color: rgba(128, 128, 128, 0.404);
  z-index: -1;
}

.menu-two {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(128, 128, 128, 0.404);
  z-index: -1;
  display: none;
}

.options {
  position: relative;
  display: block;
  animation: automenu 0.4s;
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
  position: relative;
  display: block;
  animation: turnback 4s;
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
</style>
