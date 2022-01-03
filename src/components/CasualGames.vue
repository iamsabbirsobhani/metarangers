<template>
  <div class="casual-games">
    <div class="top">
      <div class="container">
        <div class="container-wrapper">
          <div class="casual-left">
            <img
              src="../assets/casual-games/text-casual-games.png"
              alt="Casual Games"
            />
            <p>
              Casual games are an easy-to-play, easy-to-earn games. Everyone can
              start to join our metaverse by playing these game in order to
              collect Runes and PS token for other activities.
            </p>
          </div>
          <div class="casual-right">
            <img
              src="../assets/casual-games/homeplay-banner.webp"
              alt="Homeplay Banner"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="bottom-container">
        <div class="bottom-wrapper">
          <img src="../assets/casual-games/lodging_banner.webp" alt="" />
          <div>
            <img src="../assets/casual-games/text-logging.png" alt="" />
            <p>
              Logging is the very first release in the casual games series. It
              is a game for everyone because of it's simple mechanic: easy to
              play and easy to earn.
            </p>
            <br />
            <p>
              Players may join in casual games with their own Paragon using
              tools to hack down trees in the maps to earn Runes
            </p>
            <br />
            <p>
              The game employs Merkle Tree technology from the blockchain to
              ensure that the data in the game is transparent and public, and
              that players may check their progress and data at any time.
            </p>
            <br />
            <p>Have fund and earn tokens on Logging!</p>
            <div class="gvc-info__button">
              <button class="sc-furwcr bcStCS claim">coming soon</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@font-face {
  font-family: "Upheaval TT -BRK-";
  font-style: normal;
  font-weight: normal;
  src: local("Upheaval TT -BRK-"),
    url("../../public/upheavtt.woff") format("woff");
}
$pixel-font: "Upheaval TT -BRK-";

.casual-games {
  font-family: $pixel-font;
  color: white;
  max-width: 1300px;
  margin: 20px auto;
}
.bottom {
  position: relative;
  top: -190px;
  z-index: -1;
}
.bottom-wrapper {
  padding: 20px;
  justify-content: space-around;
  align-items: center;
  button {
    width: 150px;
    margin: 20px 0;
    z-index: 10;
  }
}

.container-wrapper {
  padding: 20px;
  align-items: center;
  justify-content: space-around;
  .casual-left {
    max-width: 600px;
    p {
      margin-left: 5px;
    }
  }
}

.bcStCS.claim {
  color: rgb(255, 255, 255);
  cursor: pointer;
  font-size: 18px;
  line-height: 16px;
  font-weight: 600;
  font-family: upheaval;
  width: 154px;
  height: 40px;
  text-align: left;
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  padding: 8px 15px 12px 25px;
  border-radius: 5px;
  background: url("../assets/casual-games/buttonbg.png") 0% 0% / 100% 100%
    no-repeat;
  background-repeat: no-repeat;
}
.bcStCS {
  padding: 8px 15px;
  color: rgb(255, 255, 255);
  cursor: pointer;
  font-size: 1rem;
  text-shadow: rgb(62 64 224) 2px 2px;
  letter-spacing: 0.5px;
}

.bcStCS.claim:hover,
.bcStCS.claim:active,
.bcStCS.claim:focus {
  width: 154px;
  height: 40px;
  background: url("../assets/casual-games/buttonbg-2.png") 0% 0% / 100% 100%
    no-repeat;
  background-repeat: no-repeat;
}

.container-wrapper {
  display: flex;
}
.bottom-wrapper {
  display: flex;
  background: url("../assets/casual-games/bg-game-view.webp") 0% 0% / 100% 100%
    no-repeat;
  background-repeat: no-repeat;
}

@media (max-width: 768px) {
  .top {
    max-width: 350px;
    margin: auto;
  }
  #app > div.home > div.casual-games > div.bottom > div > div {
    padding: 10px;
  }
  #app > div.home > div.casual-games > div.bottom > div > div > div {
    font-size: 18px;
    padding: 10px;
  }
  #app > div.home > div.casual-games > div.bottom > div > div > div > div {
    width: 150px;
    margin: 20px auto;
  }
  .bottom {
    max-width: 350px;
    margin: auto;
  }
  .bottom {
    position: relative;
    top: unset;
    z-index: 1;
  }
  .container-wrapper {
    flex-direction: column;
  }
  .bottom-wrapper {
    flex-direction: column;
    background: url("../assets/casual-games/bg-game-view-mobile.png") 0% 0% /
      100% 100% no-repeat;
    background-repeat: no-repeat;
  }
}
</style>
