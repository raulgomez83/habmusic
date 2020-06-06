<template>
  <div>
    <div>
      <ul>
        <li v-for="artist in artists" :key="artist.id">
          <a :href="artist.url">{{artist.name}}</a>
          <img :src="artist.image[2]['#text']" />
          {{artist.listeners}} listeners
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "artists",
  props: {
    artists: Array
  }
};
</script>


<style scoped>
li {
  width: 10rem;
}
</style>
