<template>
  <div class="card">
    <div class="card-item" v-for="(item,index) in 10" :key="index">
      <div class="card-item-top">
        <div class="card-item-top-left">
          <span class="card-item-top-left-title">Yun Zhang</span>
          <span class="card-item-top-left-text vertical-2">天中国药科大学(本科) 复旦大学（研究生） 药学</span>
        </div>
        <img src="@/assets/imgs/pcpage5/p1.png" class="card-item-top-img" />
      </div>

      <span class="card-item-title vertical-1">OFFER：普华永道、安永、强生、中银基金</span>
      <span
        class="card-item-text vertical-3"
      >感言：辅导学员遍布欧美顶尖学府麻省理工,英国剑桥大学,芝加哥大学,宾夕法尼亚大学,哥伦比亚大学等众多欧美国顶尖名校。中学生生涯规划公益性平台-盈途教育创始人,长期致力于高中生升学规划</span>
    </div>
  </div>
</template>


<script>
export default {
  name: "index",
  data() {
    return {};
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

  .card-item {
    margin-bottom: 22px;
    padding: 30px 30px 28px 30px;
    display: flex;
    flex-direction: column;
    margin-left: 22px;
    width: 494px;
    height: 296px;
    background: rgba(255, 255, 255, 1);
    border-radius: 6px;
    .card-item-top {
      display: flex;
      justify-content: space-between;
      .card-item-top-left {
        display: flex;
        flex-direction: column;
        .card-item-top-left-title {
          font-size: 24px;
          font-family: PingFangSC-Medium, PingFang SC;
          font-weight: bold;
          color: rgba(51, 51, 51, 1);
          line-height: 33px;
        }
        .card-item-top-left-text {
          margin-top: 10px;
          width: 204px;
          height: 60px;
          font-size: 18px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(119, 119, 119, 1);
          line-height: 30px;
        }
      }
      .card-item-top-img {
        width: 180px;
        height: 100px;
      }
    }
    .card-item-title {
      font-size: 18px;
      font-family: PingFangSC-Medium, PingFang SC;
      font-weight: bold;
      color: rgba(51, 51, 51, 1);
      line-height: 25px;
      margin-top: 25px;
    }
    .card-item-text {
      font-size: 14px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: rgba(153, 153, 153, 1);
      line-height: 26px;
      margin-top: 4px;
    }
  }
}
</style>