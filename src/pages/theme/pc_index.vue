<template>
  <div style="min-width:1340px">
    <pcHeader @getActiveIndex="setActiveItem" />
    <page1 v-show="activeIndex==='1'" />
    <page2 v-show="activeIndex==='2'" />
    <page3 v-show="activeIndex==='3'" />
    <page4 v-show="activeIndex==='4'" />
    <page5 v-show="activeIndex==='5'" />
    <pcBottom />
  </div>
</template>


<script>
import { mapState } from "vuex";
import pcHeader from "./components/pc/pcHeader.vue";
import pcBottom from "./components/pc/pcBottom.vue";
import page1 from "./components/pc/page1.vue";
import page2 from "./components/pc/page2.vue";
import page3 from "./components/pc/page3.vue";
import page4 from "./components/pc/page4.vue";
import page5 from "./components/pc/page5.vue";

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
    page2,
    page3,
    page4,
    page5
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