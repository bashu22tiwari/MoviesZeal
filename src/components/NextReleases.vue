<template>
  <div class="nextReleasesContainer">
    <div class="videoContainer">
      <video autoplay muted loop src="../assets/video.mp4"></video>
    </div>

    <div class="containerReleases">
      <h1>The Bill Gates Code</h1>
      <p>
        Take a trip inside the mind of Bill Gates as the billionaire opens up
        about those who influenced him and the audacious goals he's still pursuing.
      </p>
      <button id="buttonPlay">
        <v-icon name="play" scale="1" id="iconMain" color="#e5e5e5" />
        <span>To watch</span>
      </button>
      <button id="buttonInfo">
        <v-icon name="info-circle" scale="1" id="iconMain" color="#e5e5e5" />
        <span>More information</span>
      </button>
    </div>
  </div>
</template>

<script>
import Icon from "vue-awesome/components/Icon";
export default {
  name: "NextRealeses",
  data() {
    return {};
  },
  components: {
    "v-icon": Icon
  }
};
</script>
<style >
.nextReleasesContainer {
  width: 100%;
  height: 500px;
  position: relative;
  background: #1414147e;
  display: flex;
  align-items: center;
}
.nextReleasesContainer > .videoContainer {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  width: 100%;
  height: 99%;
  overflow: hidden;
}
.nextReleasesContainer > .videoContainer > video {
  width: 100%;
}
.containerReleases {
  width: 500px;
  margin-left: 40px;
}
.containerReleases h1 {
  color: #ffffff;
  text-shadow: black 0.1em 0.1em 0.2em;
  font-size: 50px;
  font-family: Arial, Helvetica, sans-serif;
  margin-bottom: 30px;
  position: relative;
}
.containerReleases p {
  color: #e9e9e9;
  font-family: Arial, Helvetica, sans-serif;
  text-shadow: #e9e9e9 0em 0em 0em;
  font-size: 15px;
  margin-bottom: 30px;
  text-align: justify;
}
.containerReleases button {
  border: none;
  background: rgba(78, 78, 78, 0.562);
  color: #e9e9e9;
  font-size: 15px;
  font-weight: bold;
  text-align: center;
  transition: transform 0.5s;
}
.containerReleases button:hover {
  border: none;
  background: rgb(255, 255, 255);
  color: #141414;
  transform: scale(1.1);
  cursor: pointer;
}
.containerReleases button span {
  padding-left: 10px;
}
#buttonPlay {
  width: 150px;
  height: 30px;
  margin-right: 20px;
}
#buttonInfo {
  width: 190px;
  height: 30px;
}
</style>
