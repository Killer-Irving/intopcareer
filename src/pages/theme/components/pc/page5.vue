<template>
  <div class="bgcf8">
    <div class="post-bg"></div>

    <div class="page5-body">
      <div class="left">
        <span class="left-title">成功学徒</span>
        <div
          @click="()=>{activeCardIndex=index}"
          v-for="(item,index) in cardsheet"
          :key="item"
          class="left-item"
          :style="{color:activeCardIndex===index?'#0855CA':'#333333'}"
        >
          <span>{{item}}</span>
          <span :style="{color:activeCardIndex===index?'#0855CA':'white'}">></span>
        </div>
      </div>

      <div class="right">
        <card1 v-show="activeCardIndex===0" />
        <card2 v-show="activeCardIndex===1" />
        <card3 v-show="activeCardIndex===2" />
      </div>
    </div>
    <!-- ** -->
  </div>
</template>


<script>
import card1 from "./page5Card/card1.vue";
import card2 from "./page5Card/card2.vue";
import card3 from "./page5Card/card3.vue";
export default {
  name: "page",
  data() {
    return {
      cardsheet: ["成功学徒", "学徒收获", "学徒风采"],
      activeCardIndex: 0
    };
  },
  props: {},
  components: {
    card1,
    card2,
    card3
  },
  mounted() {},
  created() {},
  computed: {},
  watch: {},
  methods: {}
};
</script>
<style lang="scss" scoped>
.post-bg {
  height: 520px;
  width: 100%;
  background: url("../../../../assets/imgs/pcpage5/post.png") no-repeat center 0 /
    cover;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.page5-body {
  display: flex;
  justify-content: space-between;
  padding-top: 56px;
  padding-bottom: 80px;
  margin: 0 auto;
  width: 1180px;
  .left {
    flex-shrink: 0;
    width: 120px;
    display: flex;
    flex-direction: column;
    margin-right: 23px;
    .left-title {
      font-size: 18px;
      font-family: PingFangSC-Medium, PingFang SC;
      font-weight: bold;
      color: rgba(51, 51, 51, 1);
      line-height: 25px;
      margin-bottom: 27px;
      text-align: center;
    }
    .left-item {
      cursor: pointer;
      height: 45px;
      font-size: 16px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      line-height: 45px;
      border-top: 1px solid #d8d8d8;
      text-align: center;
    }
  }
}
</style>