<template>
  <div>
    <div class="post-bg"></div>

    <div class="part1">
      <span class="part1-title">生涯规划专家团队</span>
      <div class="part1-line">
        <div
          v-for="(item,index) in 8"
          :key="index"
          class="part1-line-item"
          @mouseenter="()=>{part1ActiveIndex=index}"
          @mouseleave="()=>{part1ActiveIndex=''}"
        >
          <div class="part1-line-item-shadow"></div>
          <img
            class="part1-line-img"
            src="@/assets/imgs/pcpage4/p1.png"
            :style="{filter:part1ActiveIndex===index?'blur(10px)':''}"
          />
          <span class="part1-line-text1">蒋玲</span>
          <span class="part1-line-text2">Amy Jiang</span>

          <div class="part1-line-fake-bg" v-if="part1ActiveIndex===index">
            <span class="part1-line-fake-bg-text1">·教育部优秀创新创业导师</span>
            <span
              class="part1-line-fake-bg-text2"
            >国内多所知名大学的职业规划顾问，受邀在多所知名高校开设创新创业教育相关的讲座，国内知名商学院长期受邀讲师</span>
            <span class="part1-line-fake-bg-text1">·国内知名规划指导专家</span>
            <span
              class="part1-line-fake-bg-text2"
            >创立大学生“双轨计划”，《大学就该这么读-关键人生职业规划课》第一作者，帮助多家名企完成人才招聘及效果评估，熟悉企业招聘流程与人才能力模型，超过15年学业、职业规划经验，擅长性格分析、能力提升训练、求职文书、面试辅导等模块</span>
          </div>
        </div>
      </div>
    </div>

    <div class="part2">
      <span class="part2-title">部分资深授课老师团队</span>
      <div class="part2-line">
        <div
          v-for="(item,index) in 4"
          :key="index"
          class="part2-line-item"
          @mouseenter="()=>{part2ActiveIndex=index}"
          @mouseleave="()=>{part2ActiveIndex=''}"
        >
          <div class="part2-line-item-shadow"></div>
          <img
            class="part2-line-img"
            src="@/assets/imgs/pcpage4/p1.png"
            :style="{filter:part2ActiveIndex===index?'blur(10px)':''}"
          />
          <span class="part2-line-text1">蒋玲</span>
          <span class="part2-line-text2">Amy Jiang</span>

          <div class="part2-line-fake-bg" v-if="part2ActiveIndex===index">
            <span class="part2-line-fake-bg-text1">·教育部优秀创新创业导师</span>
            <span
              class="part2-line-fake-bg-text2"
            >国内多所知名大学的职业规划顾问，受邀在多所知名高校开设创新创业教育相关的讲座，国内知名商学院长期受邀讲师</span>
            <span class="part2-line-fake-bg-text1">·国内知名规划指导专家</span>
            <span
              class="part2-line-fake-bg-text2"
            >创立大学生“双轨计划”，《大学就该这么读-关键人生职业规划课》第一作者，帮助多家名企完成人才招聘及效果评估，熟悉企业招聘流程与人才能力模型，超过15年学业、职业规划经验，擅长性格分析、能力提升训练、求职文书、面试辅导等模块</span>
          </div>
        </div>
      </div>
    </div>

    <div class="part3">
      <span class="part3-title">部分优秀行业导师团队</span>
      <div class="part3-line">
        <div class="part3-line-item" v-for="(item,index) in 6" :key="index">
          <div class="part3-line-item-title">Amy Jiang</div>
          <span
            class="part3-line-item-text"
          >上海交通大学金融专业，毕业时拿到德勤monitor、埃克森美孚、西门子、安永、毕马威、上海银行等10家公司offer，现就职于德勤Monitor，任高级咨询顾问。</span>
        </div>
      </div>
    </div>

    <div class="part3" style="background:rgba(248,248,248,1);">
      <span class="part3-title">部分企业精英导师团队</span>
      <div class="part3-line">
        <div class="part3-line-item" v-for="(item,index) in 6" :key="index">
          <div class="part3-line-item-title">Amy Jiang</div>
          <span
            class="part3-line-item-text"
          >上海交通大学金融专业，毕业时拿到德勤monitor、埃克森美孚、西门子、安永、毕马威、上海银行等10家公司offer，现就职于德勤Monitor，任高级咨询顾问。</span>
        </div>
      </div>
    </div>

    <div class="part3">
      <span class="part3-title">部分成长教练团队</span>
      <div class="part3-line">
        <div class="part3-line-item" v-for="(item,index) in 6" :key="index">
          <div class="part3-line-item-title">Amy Jiang</div>
          <span
            class="part3-line-item-text"
          >上海交通大学金融专业，毕业时拿到德勤monitor、埃克森美孚、西门子、安永、毕马威、上海银行等10家公司offer，现就职于德勤Monitor，任高级咨询顾问。</span>
        </div>
      </div>
    </div>
    <!-- ** -->
  </div>
</template>


<script>
export default {
  name: "page",
  data() {
    return {
      part1ActiveIndex: "",
      part2ActiveIndex: ""
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
.post-bg {
  height: 520px;
  width: 100%;
  background: url("../../../../assets/imgs/pcpage4/post.png") no-repeat center 0 /
    cover;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.part1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 72px;
  padding-bottom: 120px;
  .part1-title {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
    line-height: 50px;
    margin-bottom: 40px;
  }
  .part1-line {
    width: 1180px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .part1-line-item {
      position: relative;
      margin-top: 20px;
      width: 280px;
      height: 360px;
      .part1-line-item-shadow {
        width: 280px;
        height: 80px;
        background: linear-gradient(
          180deg,
          rgba(0, 0, 0, 0) 0%,
          rgba(0, 0, 0, 0.7) 100%
        );
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: 2;
      }
      .part1-line-img {
        width: 280px;
        height: 360px;
      }
      .part1-line-text1 {
        position: absolute;
        bottom: 42px;
        left: 20px;
        font-size: 21px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(255, 255, 255, 1);
        z-index: 3;
      }
      .part1-line-text2 {
        position: absolute;
        z-index: 3;
        bottom: 20px;
        left: 20px;
        width: 80px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(255, 255, 255, 1);
      }
      .part1-line-fake-bg {
        display: flex;
        padding-top: 16px;
        flex-direction: column;
        position: absolute;
        z-index: 4;
        width: 280px;
        height: 360px;
        top: 0;
        left: 0;
        padding: 0 18px;
        background: linear-gradient(
          180deg,
          rgba(0, 0, 0, 0.1) 0%,
          rgba(0, 0, 0, 0.8) 100%
        );
        .part1-line-fake-bg-text1 {
          margin-top: 20px;
          font-size: 14px;
          font-family: PingFangSC-Semibold, PingFang SC;
          font-weight: 600;
          color: rgba(255, 255, 255, 1);
          line-height: 20px;
          margin-top: 20px;
        }
        .part1-line-fake-bg-text2 {
          margin-top: 4px;
          font-size: 14px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(255, 255, 255, 1);
          line-height: 22px;
        }
      }
    }
  }
}

.part2 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 72px;
  padding-bottom: 120px;
  background: rgba(248, 248, 248, 1);
  .part2-title {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
    line-height: 50px;
    margin-bottom: 40px;
  }
  .part2-line {
    width: 1180px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .part2-line-item {
      position: relative;
      margin-top: 20px;
      width: 280px;
      height: 360px;
      .part2-line-item-shadow {
        width: 280px;
        height: 80px;
        background: linear-gradient(
          180deg,
          rgba(0, 0, 0, 0) 0%,
          rgba(0, 0, 0, 0.7) 100%
        );
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: 2;
      }
      .part2-line-img {
        width: 280px;
        height: 360px;
      }
      .part2-line-text1 {
        position: absolute;
        bottom: 42px;
        left: 20px;
        font-size: 21px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(255, 255, 255, 1);
        z-index: 3;
      }
      .part2-line-text2 {
        position: absolute;
        z-index: 3;
        bottom: 20px;
        left: 20px;
        width: 80px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(255, 255, 255, 1);
      }
      .part2-line-fake-bg {
        display: flex;
        padding-top: 16px;
        flex-direction: column;
        position: absolute;
        z-index: 4;
        width: 280px;
        height: 360px;
        top: 0;
        left: 0;
        padding: 0 18px;
        background: linear-gradient(
          180deg,
          rgba(0, 0, 0, 0.1) 0%,
          rgba(0, 0, 0, 0.8) 100%
        );
        .part2-line-fake-bg-text1 {
          margin-top: 20px;
          font-size: 14px;
          font-family: PingFangSC-Semibold, PingFang SC;
          font-weight: 600;
          color: rgba(255, 255, 255, 1);
          line-height: 20px;
          margin-top: 20px;
        }
        .part2-line-fake-bg-text2 {
          margin-top: 4px;
          font-size: 14px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(255, 255, 255, 1);
          line-height: 22px;
        }
      }
    }
  }
}

.part3 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 72px;
  padding-bottom: 120px;
  .part3-title {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
    line-height: 50px;
  }
  .part3-line {
    margin-top: 20px;
    width: 1180px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .part3-line-item {
      margin-top: 40px;
      width: 365px;
      .part3-line-item-title {
        background: url("../../../../assets/imgs/pcpage4/post.png") no-repeat
          center 0 / cover;
        height: 38px;
        padding-left: 20px;
        font-size: 18px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(255, 255, 255, 1);
        line-height: 38px;
        margin-bottom: 16px;
      }
      .part3-line-item-text {
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(119, 119, 119, 1);
        line-height: 30px;
      }
    }
  }
}
</style>