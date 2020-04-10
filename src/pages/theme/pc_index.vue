<template>
  <div style="min-width:1340px">
    <pcHeader />
    <page1 />
  </div>
</template>


<script>
import { mapState } from "vuex";
import pcHeader from "./components/pc/pcHeader.vue";
import page1 from "./components/pc/page1.vue";

export default {
  name: "PcIndex",
  data() {
    return {};
  },
  props: {},
  components: {
    pcHeader,
    page1
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
</style>