<template>
  <div class="card">
    <div class="card-item" v-for="item in cardArr" :key="item.title">
      <img :src="item.img" class="card-item-img" />
      <span class="card-item-text">{{item.title}}</span>
    </div>
  </div>
</template>


<script>
const p21 = require("@/assets/imgs/pcpage5/p21.png");
const p22 = require("@/assets/imgs/pcpage5/p22.png");
const p23 = require("@/assets/imgs/pcpage5/p23.png");
const p24 = require("@/assets/imgs/pcpage5/p24.png");
const p25 = require("@/assets/imgs/pcpage5/p25.png");
const p26 = require("@/assets/imgs/pcpage5/p26.png");
const p27 = require("@/assets/imgs/pcpage5/p27.png");
const p28 = require("@/assets/imgs/pcpage5/p28.png");
const p29 = require("@/assets/imgs/pcpage5/p29.png");
const p30 = require("@/assets/imgs/pcpage5/p30.png");
const p31 = require("@/assets/imgs/pcpage5/p31.png");
const p32 = require("@/assets/imgs/pcpage5/p32.png");
export default {
  name: "index",
  data() {
    return {
      cardArr: [
        { title: "全面深入的性格优势挖掘", img: p21 },
        { title: "系统权威的职业能力评估", img: p22 },
        { title: "量身打造的背景提高方案", img: p23 },
        { title: "权威独到的考研规划指导", img: p24 },
        { title: "尖端一流的留学咨询服务", img: p25 },
        { title: "高效及时的笔试面试辅导", img: p26 },
        { title: "精准契合的企业实习推荐", img: p27 },
        { title: "详尽独到的求职技能课程", img: p28 },
        { title: "贴心持续的金牌教练陪伴", img: p29 },
        { title: "专业严谨的成长导师引导", img: p30 },
        { title: "丰富多元的全职职位邀约", img: p31 },
        { title: "高端卓越的职场精英人脉", img: p32 }
      ]
    };
  },
  props: {},
  components: {},
  mounted() {},
  created() {},
  computed: {},
  watch: {},
  methods: {}
};
</script>
<style lang="scss" scoped>
.card {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 1058px;
  margin-left: 22px;
  .card-item {
    width: 33%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    .card-item-img {
      margin-top: 4px;
      width: 50px;
      height: 50px;
    }
    .card-item-text {
      margin-top: 10px;
      margin-bottom: 60px;
      font-size: 18px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: rgba(51, 51, 51, 1);
      line-height: 40px;
    }
  }
}
</style>