<template>
  <transition name="fade">
    <div v-if="show" class="preloader">
      <div class="divImg">
        <img class="logoPreloader" :src="image" />
      </div>
      <Spinner />
    </div>
  </transition>
</template>

<script>
import Spinner from "../components/Spinner";
import image from "../assets/main-screen-logo.png";
export default {
  name: "Preloader",
  data() {
    return {
      show: true,
      image: image
    };
  },
  mounted() {
    if (this.show) this.showToggle();
  },
  components: {
    Spinner
  },
  methods: {
    showToggle() {
      setTimeout(() => {
        this.show = false;
        this.$router.push("/Main");
      }, 4000);
    }
  }
};
</script>

<style>
.preloader {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #141414;
  z-index: 9999;
}
.divImg {
  width: 100%;
  margin-top: -40px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
