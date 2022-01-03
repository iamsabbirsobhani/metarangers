<template>
  <div class="team-container">
    <img
      class="text-team"
      src="../assets/team/img-text-team.webp"
      alt="text-team"
    />
    <div class="team">
      <div class="team-individual">
        <div class="individual">
          <img :src="individualTeam.url" :alt="individualTeam.alt" />
          <p>{{ individualTeam.skill }}</p>
        </div>
      </div>
      <div
        class="team-all"
        :class="gridStyle ? `grid grid-cols-4 gap-4` : `grid grid-cols-2 gap-4`"
      >
        <div v-for="team in teams" :key="team.id" class="teams">
          <div class="imgbtn" @click="onClick(team.id)">
            <img :src="team.url" :alt="team.alt" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";
import { onMounted } from "@vue/runtime-core";
const gridStyle = ref(true);
const teams = ref([
  {
    id: 0,
    url: new URL("../assets/team/team-louis-nguyen.webp", import.meta.url).href,
    alt: "louis-nguyen",
    skill: `5+ years of experience in Blockchain and Fintech`,
  },
  {
    id: 1,
    url: new URL("../assets/team/team-bui-ba-hien.webp", import.meta.url).href,
    alt: "bui-ba-hien",
    skill: `CEO Box Studio 10 years of experience in Marketing and Gaming`,
  },
  {
    id: 2,
    url: new URL("../assets/team/team-tran-diep.webp", import.meta.url).href,
    alt: "tran-diep",
    skill: `MKT Lead FPT Online, VTC Online Social Media Manager VTVlive - VTVCab MKT Manager Funtap JSC`,
  },
  {
    id: 3,
    url: new URL("../assets/team/team-hung-hoang-viet.webp", import.meta.url)
      .href,
    alt: "hung-hoang-viet",
    skill: `Co-Founder Sparta VFX`,
  },
  {
    id: 4,
    url: new URL("../assets/team/team-dau-ngoc-huy.webp", import.meta.url).href,
    alt: "dau-ngoc-huy",
    skill: `Former Creative Director K14, VCCorp`,
  },
  {
    id: 5,
    url: new URL("../assets/team/team-peter-hamachan.webp", import.meta.url)
      .href,
    alt: "peter-hamachan",
    skill: `10 years of experience in Development and 4 years of experience in Blockchain`,
  },
  {
    id: 6,
    url: new URL("../assets/team/team-tony-bennett.webp", import.meta.url).href,
    alt: "tony-bennett",
    skill: `10 years of experience in Development and 4 years of experience in Blockchain`,
  },
]);
const individualTeam = ref();
individualTeam.value = teams.value[0];
const onClick = (id) => {
  individualTeam.value = teams.value[id];
};
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
.team-container {
  margin: 100px auto;
  font-family: $pixel-font;
}
.team {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 30px;
}
.imgbtn {
  cursor: pointer;
}
.individual {
  p {
    padding: 5px;
    width: 357px;
    margin: 10px auto;
    color: white;
    font-size: 20px;
  }
}
.team-individual {
  width: 700px;
}
.text-team {
  margin: auto;
  max-width: 35rem;
}
@media (max-width: 764px) {
  .team {
    flex-direction: column;
  }
  .individual {
    max-width: 310px;
    margin: 20px auto;
  }
  .teams {
    max-width: 170px;
  }
  .text-team {
    margin: auto;
    max-width: 20rem;
  }
  .team-individual {
    width: 310px;
  }
}
</style>
