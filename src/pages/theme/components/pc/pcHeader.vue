<template>
  <div class="pc-tab">
    <img src="@/assets/imgs/logo.png" class="logo-img" />
    <div class="f">
      <div v-for="(item,index) in entry" :key="index">
        <span
          @click="setActiveIndex(item.value)"
          :class="[
              'title-item',
              activeValue === item.value&&item.value!=='1' ? 'title-item-active' : '' ,
              activeValue === item.value&&item.value==='1' ? 'title-item-active-page1' : '' ,
            ]"
        >{{item.title}}</span>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "pcHeader",
  data() {
    return {
      entry: [
        { title: "首页", value: "1" },
        { title: "双轨计划", value: "2" },
        { title: "优职计划", value: "3" },
        { title: "师资力量", value: "4" },
        { title: "成功学徒", value: "5" },
        { title: "关于我们", value: "6" }
      ],
      activeValue: "1"
    };
  },
  props: {},
  components: {},
  mounted() {},
  created() {
    this.setActiveIndex(sessionStorage.getItem("activeIndex") || "1");
  },
  computed: {},
  watch: {},
  methods: {
    setActiveIndex(index) {
      this.activeValue = index;
      sessionStorage.setItem("activeIndex", index);
      this.$emit("getActiveIndex", index);
    }
  }
};
</script>
<style lang="scss" scoped>
.pc-tab {
  height: 90px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 368px 0 370px;
  z-index: 3;
  background: white;
}
.pc-tab-fixed {
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
}
.logo-img {
  width: 244px;
  height: 80px;
  margin-top: -10px;
}
.title-item {
  cursor: pointer;
  height: 90px;
  margin-right: 32px;
  font-size: 16px;
  font-family: PingFangSC-Regular, PingFang SC;
  font-weight: 400;
  color: rgba(51, 51, 51, 1);
}
.title-item-active-page1 {
  font-weight: 600;
  padding-bottom: 8px;
  color: white;
  border-bottom: 2px solid white;
}
.title-item-active {
  font-weight: 600;
  padding-bottom: 8px;
  color: rgba(8, 85, 202, 1);
  border-bottom: 2px solid #0855ca;
}
</style>