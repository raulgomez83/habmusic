<template>
  <div>
    <vue-headful title="TopArtists" />
    <artists :artists="artists"></artists>
    <FooterCustom></FooterCustom>
  </div>
</template>

<script>
import api from "@/api/index.js";
import artists from "@/components/artists.vue";
import FooterCustom from "@/components/FooterCustom.vue";
export default {
  name: "Topartist",
  components: {
    artists,
    FooterCustom
  },
  data() {
    return {
      artists: []
    };
  },
  created() {
    api;
    api
      .getArtists()
      .then(response => (this.artists = response.data.topartists.artist));
  }
};
</script>

<style>
</style>