<template>
  <div id="app">
    <NextReleases />
    <Movies :key="movie.id" :type="movie.type" v-for="movie in movies"/>
    <h4>Movies Zeal App - Bashu Tiwari</h4>
    <h4>Email : bashutiwariapsg22@gmail.com</h4>
  </div>
</template>

<script>
import NextReleases from "../components/NextReleases";
import Movies from "../components/Movies";

export default {
  name: "App",
  components: {
    NextReleases,
    Movies,
  },
  computed: {
    movies() {
      return [
        {id: 1, type: "s=avengers", description: "Popular On Netflix"},
        {id: 2, type: "s=harry", description: "Recommended"},
        {id: 3, type: "s=fast", description: "High Demand"},
        {id: 4, type: "s=super", description: "Adventure"},
        {id: 5, type: "s=game", description: "Fiction"},
        {id: 6, type: "s=brain", description: "For All Ages"},
        {id: 7, type: "s=all", description: "Family"}
      ]
    }
  }
};
</script>

<style>
#app h4 {
  color: #e9e9e9;
  text-align: center;
  font-family: Arial, Helvetica, sans-serif;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
