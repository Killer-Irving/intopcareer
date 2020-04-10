<template>
  <div style="min-width:1340px">
    <pcHeader @getActiveIndex="setActiveItem" />
    <page1 v-if="activeIndex==='1'" />
    <page2 v-if="activeIndex==='2'" />
    <pcBottom />
  </div>
</template>


<script>
import { mapState } from "vuex";
import pcHeader from "./components/pc/pcHeader.vue";
import pcBottom from "./components/pc/pcBottom.vue";
import page1 from "./components/pc/page1.vue";
import page2 from "./components/pc/page2.vue";

export default {
  name: "PcIndex",
  data() {
    return {
      activeIndex: "1"
    };
  },
  props: {},
  components: {
    pcHeader,
    pcBottom,
    page1,
    page2
  },
  mounted() {},
  created() {},
  computed: {
    ...mapState({
      theme: state => state.theme
    })
  },
  watch: {},
  methods: {
    setActiveItem(e) {
      this.activeIndex = e;
    }
  }
};
</script>
<style lang="scss" scoped>
</style>