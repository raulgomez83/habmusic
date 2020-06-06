<template>
  <div>
    <div>
      <ul>
        <li v-for="track in tracks" :key="track.id">
          <a :href="track.url">{{ track.name }}</a>
          <p>{{ track.listeners }} listeners</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "tracks",
  props: {
    tracks: Array,
  },
};
</script>

<style scoped>
li {
  width: 8rem;
  height: 9rem;
}
</style>
