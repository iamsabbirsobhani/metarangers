<template>
  <div class="super-airdrop">
    <img class="bg-rectangle" src="../assets/super-airdrop/bg-rectangle-1.png" alt="">
    <div class="img-super-airdrop">
      <img src="../assets/super-airdrop/superAirdrop.png" alt="" />
      <p class="text-center text-white my-5 text-lg">
        55,000 PRL + $1,500 will be distributed for participants on Super
        Listing Event. Don't miss your chance!
      </p>
    </div>
    <div class="air-box">
      <div class="air-box-1 ab">
        <img class="lock" src="../assets/super-airdrop/air-lock-1.png" alt="" />
        <h3>SHARE TEASER</h3>
        <h3>EARN PRL</h3>
        <div class="prl">
          <h4>10,000&nbsp;</h4>
          <img src="../assets/super-airdrop/prl.png" alt="" />
          <h4>&nbsp;+&nbsp;$500</h4>
        </div>
        <p>Share our super teaser video on Facebook/Twitter</p>
        <div class="hac-button">
          <a href="#" target="_blank" rel="noreferrer"
            ><button class="sc-jrQzAO fEZBZB square">join now</button></a
          >
        </div>
      </div>
      <div class="air-box-2 ab">
        <img class="lock" src="../assets/super-airdrop/air-lock-2.png" alt="" />
        <h3>SHARE NOW</h3>
        <h3>EARN NOW</h3>
        <div class="prl">
          <h4>20,000&nbsp;</h4>
          <img src="../assets/super-airdrop/prl.png" alt="" />
          <h4>&nbsp;+&nbsp;$1000</h4>
        </div>
        <p>Share the Super Listing Event livestream</p>
        <div class="hac-button">
          <a href="#" target="_blank" rel="noreferrer"
            ><button class="sc-jrQzAO fEZBZB square">LEARN MORE</button></a
          >
        </div>
      </div>
      <div class="air-box-3 ab">
        <img class="lock" src="../assets/super-airdrop/air-lock-3.png" alt="" />
        <h3>Squizz game</h3>
        <h3>livestream</h3>
        <div class="prl">
          <h4>20,000&nbsp;</h4>
          <img src="../assets/super-airdrop/prl.png" alt="" />
        </div>
        <p>Show your knowledge about The Parallel</p>
        <div class="hac-button">
          <a href="#" target="_blank" rel="noreferrer"
            ><button class="sc-jrQzAO fEZBZB square">LEARN MORE</button></a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";


.super-airdrop {
  position: relative;
  img {
    margin: auto;
  }
}
.bg-rectangle {
  position: absolute;
  top: 50px;
  z-index: -1;
}
.img-super-airdrop {
  position: relative;
  top: 80px;
}
.air-box {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 50px 0;
}
.ab {
  width: 340px;
  height: 550px;
  margin: 100px 0;
  background-size: 100% 100%;
  background-repeat: no-repeat;
}

.air-box-1 {
  background-image: url("../assets/super-airdrop/air-bg-1.webp");
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
  .lock {
    position: relative;
    bottom: 70px;
    max-width: 280px;
  }
  h3 {
    position: relative;
    bottom: 70px;
    color: #5dbeff;
    text-shadow: 0 2px 0 #3e40e0;
    letter-spacing: 0.04em;
    font-size: 35px;
    line-height: 32px;
  }
  .prl {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    bottom: 50px;
    h4 {
      text-align: center;
      color: #ffcf5b;
      letter-spacing: 0.04em;
      font-size: 20px !important;
    }
  }
  p {
    position: relative;
    bottom: 35px;
    text-align: center;
    color: white;
    font-size: 16px;
  }
  .hac-button {
    position: relative;
    bottom: 15px;
    font-family: "Upheaval TT -BRK-";
  }
  button {
    font-family: "Upheaval TT -BRK-" !important;
  }
}

.air-box-2 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-image: url("../assets/super-airdrop/air-bg-2.webp");
  padding: 20px;
  .lock {
    position: relative;
    bottom: 70px;
    max-width: 280px;
  }
  h3 {
    position: relative;
    bottom: 70px;
    color: #5dbeff;
    text-shadow: 0 2px 0 #3e40e0;
    letter-spacing: 0.04em;
    font-size: 35px;
    line-height: 32px;
  }
  .prl {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    bottom: 50px;
    h4 {
      text-align: center;
      color: #ffcf5b;
      letter-spacing: 0.04em;
      font-size: 20px !important;
    }
  }
  p {
    position: relative;
    bottom: 35px;
    text-align: center;
    color: white;
    font-size: 16px;
  }
  .hac-button {
    position: relative;
    bottom: 15px;
  }
  button {
    font-family: "Upheaval TT -BRK-" !important;
    width: 200px !important;
  }
}

.air-box-3 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-image: url("../assets/super-airdrop/air-bg-3.webp");
  padding: 20px;
  .lock {
    position: relative;
    bottom: 70px;
    max-width: 280px;
  }
  h3 {
    position: relative;
    bottom: 70px;
    color: #5dbeff;
    text-shadow: 0 2px 0 #3e40e0;
    letter-spacing: 0.04em;
    font-size: 35px;
    line-height: 32px;
  }
  .prl {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    bottom: 50px;
    h4 {
      text-align: center;
      color: #ffcf5b;
      letter-spacing: 0.04em;
      font-size: 20px !important;
    }
  }
  p {
    position: relative;
    bottom: 35px;
    text-align: center;
    color: white;
    font-size: 16px;
  }
  .hac-button {
    position: relative;
    bottom: 15px;
  }
  button {
    font-family: "Upheaval TT -BRK-" !important;
    width: 200px !important;
  }
}

.prl {
  max-width: 40px;
}

@media (max-width: 768px) {
  .air-box {
    flex-direction: column;
    justify-content: center;
  }
  .ab {
    margin: 50px 0;
  }
  .super-airdrop {
    img {
      width: 300px;
    }
  }
  .super-airdrop::before {
    content: "";
    background-image: url("../assets/super-airdrop/bg-airdrope.png");
    width: 100%;
    height: 330%;
    background-size: 100% 100%;
    z-index: -2;
    position: absolute;
    top: 160px;
    left: 0px;
  }
}

// custom stype
@media (min-width: 600px) {
  .jLPyKD .hac-detail .hac-button {
    margin-top: 20px;
  }
}
.jLPyKD .hac-detail .hac-button {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: center;
  justify-content: center;
  margin-top: 23px;
}

@media (min-width: 1200px) {
  .jLPyKD .hac-detail .hac-button button {
    width: 235px;
  }
}
@media (min-width: 600px) {
  .jLPyKD .hac-detail .hac-button button {
    width: 230px;
  }
}
.jLPyKD .hac-detail .hac-button button {
  width: 160px;
}
@media (min-width: 1200px) {
  .fEZBZB.square {
    font-size: 22px;
    line-height: 20px;
    background-size: 100% 100%;
    padding: 16px 20px 22px;
  }
}
@media (min-width: 600px) {
  .fEZBZB.square {
    font-size: 22px;
    line-height: 20px;
    padding: 14px 20px 24px;
    width: 233px;
  }
}
.fEZBZB.square {
  color: rgb(255, 255, 255);
  cursor: pointer;
  font-size: 18px;
  line-height: 20px;
  font-weight: 600;
  font-family: upheaval;
  text-align: center;
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: center;
  justify-content: center;
  width: 126px;
  border-radius: 5px;
  padding: 7px 15px 13px;
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAARgAAAA9BAMAAACEtmuOAAAAFVBMVEUAAAAAAAAAAADurEf/3aybZxnDhSYWSqa6AAAAA3RSTlMzAFy+hoLIAAAAiUlEQVRo3u3ZsQmDUBgA4T+B9Pkh6UNWCKQXHEALJxDe/iMIImhzhY0+4W6Cr7/IfLVV1GSKEbMbU8r4q6J/KWLEiBGzTQwlhhJDiaHEUGIoMZQYSgwlhhJDiaHEUGIoMZQYSgwlhhJzQCsm4jFUURch5hqYzPdQRf08TJ+xdP/OfeKUbmIugpkA43rofROe8W8AAAAASUVORK5CYII=)
    0% 0% / 100% 100% no-repeat;
  background-repeat: no-repeat;
}

@media (min-width: 1200px) {
  .jLPyKD .hac-detail .hac-button button {
    width: 235px;
  }
}
@media (min-width: 600px) {
  .jLPyKD .hac-detail .hac-button button {
    width: 230px;
  }
}

.jLPyKD .hac-detail .hac-button button {
  width: 160px;
}
@media (min-width: 1200px) {
  .fEZBZB.square:hover,
  .fEZBZB.square:active,
  .fEZBZB.square:focus {
    padding: 16px 20px 22px;
    font-size: 22px;
    line-height: 20px;
    background-size: 100% 100%;
  }
}
@media (min-width: 600px) {
  .fEZBZB.square:hover,
  .fEZBZB.square:active,
  .fEZBZB.square:focus {
    padding: 14px 20px 24px;
    font-size: 22px;
    line-height: 20px;
  }
}

.fEZBZB.square:hover,
.fEZBZB.square:active,
.fEZBZB.square:focus {
  font-size: 18px;
  line-height: 20px;
  padding: 7px 15px 13px;
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAARgAAAA5BAMAAAAfJymYAAAAD1BMVEUAAADurEf/3aybZxnDhSZLRUGTAAAAAXRSTlMAQObYZgAAAGhJREFUWMPtzrEJgEAQBdGPViBYgFiBYAXC9l+ToSYTXHJsMK+Cl2S9W7gSM2aGM1XP1sJeZcaMGTN/ZogZYoaYIWaIGWKGmCFmiBlihpghZogZYoaYIWaIGWJmgi+TLGcLR2LGzGjmBXMxxAMkDpovAAAAAElFTkSuQmCC)
    0% 0% / 100% 100% no-repeat;
  background-repeat: no-repeat;
  transition: all 0.2s ease 0s;
}
</style>
