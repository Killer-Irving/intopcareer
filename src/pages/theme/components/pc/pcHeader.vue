<template>
  <div class="pc-tab">
    <img src="@/assets/imgs/logo.png" class="logo-img" />
    <div class="f">
      <div v-for="(item,index) in entry" :key="index">
        <span
          @click="()=>{activeValue=item.value}"
          :class="[
              'title-item',
              activeValue === item.value&&item.value!=='1' ? 'title-item-active' : '' ,
            ]"
        >{{item.title}}</span>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "index",
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
  props: {
    type: {
      type: String,
      defualt: ""
    }
  },
  components: {},
  mounted() {},
  created() {},
  computed: {},
  watch: {},
  methods: {}
};
</script>
<style lang="scss" scoped>
.pc-tab {
  height: 90px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 368px 0 370px;
}
.logo-img {
  width: 178px;
  height: 50px;
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
.title-item-active {
  font-weight: 600;
  padding-bottom: 8px;
  color: rgba(8, 85, 202, 1);
  border-bottom: 2px solid #0855ca;
}
</style>