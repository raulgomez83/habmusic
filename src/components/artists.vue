<template>
  <div>
    <div>
      <ul>
        <li v-for="artist in artists" :key="artist.id">
          <a :href="artist.url">{{artist.name}}</a>
          <img :src="artist.image[2]['#text']" />
          <p>{{artist.listeners}} listeners</p>
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
p {
  color: lime;
}
img {
  opacity: 0.4;
}
</style>
