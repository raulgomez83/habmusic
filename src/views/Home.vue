<template>
  <div>
    <vue-headful title="Home" />
    <tags :tags="tags"></tags>
    <!-- Array del componente igual array de la vista -->
    <FooterCustom></FooterCustom>
  </div>
</template>

<script>
import Swal from "sweetalert2";
import api from "@/api/index.js";
import tags from "@/components/tags.vue";
import FooterCustom from "@/components/FooterCustom.vue";

export default {
  name: "Home",
  components: { tags, FooterCustom },
  data() {
    return {
      artists: [],
      tags: [],
    };
  },

  created() {
    api.getTags().then((response) => (this.tags = response.data.tags.tag));
  },
};
</script>
<style scoped></style>
