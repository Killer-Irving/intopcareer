<template>
  <div class="index-page">


  </div>
</template>


<script>
import { mapState } from "vuex";

export default {
  name: "MobleIndex",
  data() {
    return {};
  },
  props: {},
  components: {
  },
  mounted() {},
  created() {},
  computed: {
    ...mapState({
      theme: state => state.theme
    })
  },
  watch: {},
  methods: {}
};
</script>
<style lang="scss" scoped>
.index-page {
  padding-bottom: 128px;
}
</style>