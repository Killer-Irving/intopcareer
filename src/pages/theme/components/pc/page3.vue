<template>
  <div>
    <div class="post-bg">
      <span class="text2">定制你的专属用名企计划</span>
      <div class="btn-text">定制你的计划</div>
    </div>

    <div class="part1">
      <span class="text1">计划优势</span>
      <span class="text2">大学生身处考研、留学、求职，三重困局，单一选择一条路径风险高</span>
      <div class="icon-line">
        <div v-for="item in part1Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <span class="text3">{{item.title}}</span>
        </div>
      </div>
    </div>

    <div class="part2">
      <span class="text1">适宜人群</span>
      <div class="icon-line">
        <div v-for="item in part2Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <div class="middle-line"></div>
          <span class="text3">{{item.text}}</span>
        </div>
      </div>
    </div>

    <div class="part3">
      <span class="text1">定制培养流程</span>

      <div class="part3-title">
        <div class="part3-title-bg">准备阶段</div>
      </div>
      <div class="part3-zero">
        <div class="part3-zero-dotted"></div>
        <div class="part3-zero-item">
          <img class="part3-zero-item-img" src="@/assets/imgs/pcpage3/p31.png" />
          <span class="part3-zero-item-text1">报名成功</span>
        </div>
        <div class="part3-zero-solid"></div>
        <div class="part3-zero-item">
          <img class="part3-zero-item-img" src="@/assets/imgs/pcpage3/p32.png" />
          <span class="part3-zero-item-text1">匹配导师</span>
          <span class="part3-zero-item-text2">位生涯规划专家</span>
          <span class="part3-zero-item-text2">位属于您的专职成长陪伴教练</span>
        </div>
        <div class="part3-zero-dotted"></div>
      </div>

      <div class="part3-title">
        <div class="part3-title-bg">Step 1</div>
        <div class="part3-title-text">科学全面评估规划，提升大学生方向感知力</div>
      </div>
      <div class="part3-one">
        <div v-for="item in part3_2Arr" :key="item.title" class="part3-two-item">
          <img :src="item.img" class="part3-two-item-img" />
          <span class="part3-two-item-title">{{item.title}}</span>
          <span class="part3-two-item-text">{{item.text1}}</span>
          <span class="part3-two-item-text">{{item.text2}}</span>
        </div>
      </div>

      <div class="part3-title">
        <div class="part3-title-bg">Step 2</div>
        <div class="part3-title-text">打造大学生底层系统构建，提升核心竞争力</div>
      </div>
      <div class="part3-two"></div>

      <div class="part3-title">
        <div class="part3-title-bg">Step 3</div>
        <div class="part3-title-text">培养大学生通用胜任力，构建全能型人才模型</div>
      </div>
      <div class="part3-three">
        <div class="part3-three-item" v-for="item in part3_3Arr" :key="item.title">
          <div class="part3-three-item-imgdiv">
            <img :src="item.img" class="part3-three-item-img" />
          </div>
          <span class="part3-three-item-title">{{item.title}}</span>
        </div>
      </div>

      <div class="part3-title">
        <div class="part3-title-bg">Step 4</div>
        <div class="part3-title-text">专项求职技能培养，全面提升职业竞争力</div>
      </div>
      <div class="part3-four"></div>

      <div class="part3-title">
        <div class="part3-title-bg">Step 5</div>
        <div class="part3-title-text">OFFER保障</div>
      </div>
      <div class="part3-zero">
        <div class="part3-zero-dotted"></div>
        <div class="part3-zero-item">
          <img class="part3-zero-item-img" src="@/assets/imgs/pcpage3/p49.png" />
          <span class="part3-zero-item-text1">OFFER选择</span>
        </div>
        <div class="part3-zero-solid"></div>
        <div class="part3-zero-item">
          <img class="part3-zero-item-img" src="@/assets/imgs/pcpage3/p50.png" />
          <span class="part3-zero-item-text1">年薪保障</span>
        </div>
        <div class="part3-zero-dotted"></div>
      </div>
    </div>

    <div class="part4">
      <span class="text1">多对一专属服务</span>
      <span class="text2">用匠心，守初心，成就学徒名校名企梦想</span>
      <div class="loop">
        <div class="loop-item" v-for="item in part4Arr" :key="item.title">
          <img :src="item.img" class="loop-img" />
          <span class="loop-title">{{item.title}}</span>
          <span class="loop-text">{{item.text}}</span>
        </div>
      </div>
    </div>

    <div class="part6">
      <span class="text1">学徒好评</span>
      <div class="part6-bg">
        <span
          class="part6-text part6-text1"
        >我认为盈途教育在求职这一块，从理念到实践，都是比较重视和先进的机构之一，并且努力和国际接轨。一名立志进入MBB咨询公司的准大四学生，为此已经准备了近2年的时间。成为金牌学徒后，每天坚持听课+作业打卡，成为很多学员的榜样，目前已经去某家MBB咨询公司面试实习并成功斩获了Offer。</span>
        <span
          class="part6-text part6-text2"
        >在盈途，每个人通过自己的努力，一点点改变现状，积累能量，成为更好的自己。我是一名曾放弃咨询求职的海归，在意识到自己错过太多学习咨询Case的机会，面试屡遭受挫时，遇见了盈途。参加求职、笔试、面试一系列的培训后，发奋努力，坚持听课+作业打卡，重拾了求职的信心，逐渐提升了Case分析水平，简单的Case分析早已不再是问题。</span>
        <span
          class="part6-text part6-text3"
        >我是一个三分热度重度患者的大三学生。期待通过自己的努力进入咨询行业，而自己性格成了最大的绊脚石。遇到盈途教育后，坚持每天学习课程+作业打卡，不断提升自己的求职技能，磨炼自己的性格，因为我明白比我优秀的人，还比我还努力，我只有更用心，更努力，不断跟优秀的人看齐，才能收获一份更好的未来。</span>
      </div>
    </div>

    <!-- ** -->
  </div>
</template>


<script>
const p11 = require("@/assets/imgs/pcpage3/p11.png");
const p12 = require("@/assets/imgs/pcpage3/p12.png");
const p13 = require("@/assets/imgs/pcpage3/p13.png");
const p14 = require("@/assets/imgs/pcpage3/p14.png");
const p15 = require("@/assets/imgs/pcpage3/p15.png");
const p16 = require("@/assets/imgs/pcpage3/p16.png");
const p21 = require("@/assets/imgs/pcpage3/p21.png");
const p22 = require("@/assets/imgs/pcpage3/p22.png");
const p23 = require("@/assets/imgs/pcpage3/p23.png");
const p31 = require("@/assets/imgs/pcpage3/p31.png");
const p32 = require("@/assets/imgs/pcpage3/p32.png");
const p33 = require("@/assets/imgs/pcpage3/p33.png");
const p34 = require("@/assets/imgs/pcpage3/p34.png");
const p35 = require("@/assets/imgs/pcpage3/p35.png");
const p38 = require("@/assets/imgs/pcpage3/p38.png");
const p39 = require("@/assets/imgs/pcpage3/p39.png");
const p40 = require("@/assets/imgs/pcpage3/p40.png");
const p41 = require("@/assets/imgs/pcpage3/p41.png");
const p42 = require("@/assets/imgs/pcpage3/p42.png");
const p43 = require("@/assets/imgs/pcpage3/p43.png");
const p44 = require("@/assets/imgs/pcpage3/p44.png");
const p45 = require("@/assets/imgs/pcpage3/p45.png");
const p46 = require("@/assets/imgs/pcpage3/p46.png");
const p47 = require("@/assets/imgs/pcpage3/p47.png");
const p441 = require("@/assets/imgs/pcpage3/p441.png");
const p442 = require("@/assets/imgs/pcpage3/p442.png");
const p443 = require("@/assets/imgs/pcpage3/p443.png");
const p444 = require("@/assets/imgs/pcpage3/p444.png");
const p445 = require("@/assets/imgs/pcpage3/p445.png");

export default {
  name: "page",
  data() {
    return {
      part1Arr: [
        { title: "专属定制", img: p11 },
        { title: "全程陪伴", img: p12 },
        { title: "深度学习", img: p13 },
        { title: "行业赋能", img: p14 },
        { title: "竞争力构建", img: p15 },
        { title: "结果保障", img: p16 }
      ],
      part2Arr: [
        {
          text: "毕业后想进入名企的大一大二学生",
          img: p21
        },
        {
          text: "国内本科生毕业前18个月的在校生",
          img: p22
        },
        {
          text: "海外高校毕业6个月内的留学生",
          img: p23
        }
      ],
      part3_2Arr: [
        { img: p33, title: "全面评估", text: "" },
        {
          img: p34,
          title: "培养方案",
          text1: "确定培养方案",
          text2: "个性化培养服务开启"
        },
        { img: p35, title: "成长指导", text1: "自我认知", text2: "阶段沟通" }
      ],
      part3_3Arr: [
        { img: p38, title: "校园生活" },
        { img: p39, title: "背景提升" },
        { img: p40, title: "阅读计划" },
        { img: p41, title: "行业认知" },
        { img: p42, title: "实习实践" },
        { img: p43, title: "胜任力" },
        { img: p44, title: "英语训练" },
        { img: p45, title: "简历文书" },
        { img: p46, title: "笔试训练" },
        { img: p47, title: "面试表达" }
      ],
      part4Arr: [
        {
          title: "生涯规划专家",
          text:
            "拥有10年以上大学生学业、就业规划发展指导经验，熟悉学业及就业特点，指导学徒通过专业测评工具自我发现，引导规划及调整学业及职业方向，制定各阶段提升策略，解决学业及职业中方向性及关键性问题。",
          img: p441
        },
        {
          title: "资深授课老师",
          text:
            "拥有5年以上相关课程的授课经验，用浅显易懂的语言、本着以学生为主体的教学理念，注重调动和激发学生的自主性，帮助学生提升学业或就业技能。",
          img: p442
        },
        {
          title: "成长陪伴教练",
          text:
            "1V1全程学徒服务跟踪，具备超强的亲和力、责任心及洞察力，全面负责学徒建档、追踪、提升计划制定及监控，全程辅导学业、就业过程，协调各领域导师、专业团队及资源帮助学徒达成目标。",
          img: p443
        },
        {
          title: "优秀行业导师",
          text:
            "超过1000名已毕业的优秀学徒自愿加入双轨计划成为兼职行业导师。他们理解求职痛点，更懂培养规则，将感恩化作有效反哺行动，用工作经验、机会推荐和一手信息等带领后辈成长。",
          img: p444
        },
        {
          title: "名企精英导师",
          text:
            "导师来自汇丰、渣打、摩立特、BCG、普华、德勤、宝洁、玛氏、百度、腾讯、阿里等主流行业里的明星企业，将名企求职与工作经历细化分解后传递给学徒，让学徒深度理解行业背景下企业的各种细节，使职业能力提升更具针对性。",
          img: p445
        }
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
.post-bg {
  height: 520px;
  width: 100%;
  background: url("../../../../assets/imgs/pcpage3/post.png") no-repeat center 0 /
    cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  .text2 {
    margin-top: 251px;
    font-size: 24px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
  }
  .btn-text {
    cursor: pointer;
    margin-top: 50px;
    width: 180px;
    height: 44px;
    border-radius: 24px;
    border: 1px solid rgba(255, 255, 255, 1);
    font-size: 18px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(255, 255, 255, 1);
    line-height: 44px;
    text-align: center;
  }
}

.part1 {
  height: 430px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 72px;
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
    margin-bottom: 14px;
  }
  .text2 {
    font-size: 18px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(136, 136, 136, 1);
    line-height: 32px;
  }
  .icon-line {
    display: flex;
    align-items: center;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      .icon {
        width: 72px;
        height: 69px;
        margin-bottom: 21px;
      }
      .text3 {
        font-size: 22px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
      }
    }
  }
}

.part2 {
  height: 522px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgba(248, 248, 248, 1);
  padding-top: 72px;
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
  }
  .icon-line {
    display: flex;
    align-items: center;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 0 26px;
      width: 380px;
      height: 260px;
      background: linear-gradient(
        180deg,
        rgba(247, 249, 255, 1) 0%,
        rgba(255, 255, 255, 1) 100%
      );
      border: 1px solid rgba(232, 232, 232, 1);
      .icon {
        width: 56px;
        height: 56px;
      }
      .middle-line {
        width: 140px;
        height: 1px;
        background-color: #0855ca;
        margin-top: 26px;
        margin-bottom: 29px;
      }
      .text3 {
        font-size: 18px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
        line-height: 32px;
      }
    }
  }
}

.part3 {
  display: flex;
  flex-direction: column;
  padding-top: 72px;
  padding-bottom: 80px;
  align-items: center;
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
    margin-bottom: 40px;
  }
  .part3-title {
    display: flex;
    width: 1180px;
    .part3-title-bg {
      width: 171px;
      height: 72px;
      background: url("../../../../assets/imgs/pcpage3/p3.png") no-repeat center
        0 / cover;
      font-size: 28px;
      font-family: AlibabaPuHuiTiM;
      color: rgba(255, 255, 255, 1);
      text-align: center;
      padding-top: 8px;
      margin-right: 20px;
      margin-top: 60px;
    }
    .part3-title-text {
      margin-top: 60px;
      font-size: 30px;
      font-family: PingFangSC-Medium, PingFang SC;
      font-weight: 500;
      color: rgba(51, 51, 51, 1);
      line-height: 42px;
    }
  }
  .part3-zero {
    width: 1180px;
    display: flex;
    margin-bottom: 100px;
    margin-top: 80px;
    .part3-zero-item {
      width: 230px;
      margin: 0 -20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      .part3-zero-item-img {
        width: 86px;
        height: 86px;
      }
      .part3-zero-item-text1 {
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
        line-height: 28px;
        margin-top: 16px;
      }
      .part3-zero-item-text2 {
        margin-top: 6px;
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(102, 102, 102, 1);
      }
    }
    .part3-zero-dotted {
      margin-top: 42px;
      width: 299px;
      height: 1px;
      background-color: #d8d8d8;
    }
    .part3-zero-solid {
      margin-top: 42px;
      width: 330px;
      height: 1px;
      background-color: #2166d0;
    }
  }
  .part3-one {
    display: flex;
    width: 1180px;
    justify-content: space-between;
    margin-bottom: 48px;
    margin-top: 80px;
    .part3-two-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 380px;
      height: 280px;

      background: url("../../../../assets/imgs/pcpage3/p37.png") no-repeat
        center 0 / cover;
      .part3-two-item-img {
        width: 60px;
        height: 60px;
        margin-top: 65px;
        margin-bottom: 30px;
      }
      .part3-two-item-title {
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
        line-height: 28px;
        margin-bottom: 8px;
      }
      .part3-two-item-text {
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(153, 153, 153, 1);
        line-height: 24px;
      }
    }
  }
  .part3-two {
    width: 930px;
    margin-bottom: 48px;
    margin-top: 115px;
    height: 465px;
    background: url("../../../../assets/imgs/pcpage3/p36.png") no-repeat center
      0 / cover;
  }
  .part3-three {
    margin-top: 20px;
    margin-bottom: 48px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 1180px;
    .part3-three-item {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 20%;
      .part3-three-item-imgdiv {
        margin-top: 60px;
        display: flex;
        align-items: center;
        width: 100px;
        justify-content: center;
        border-radius: 50px;
        margin-bottom: 10px;
        height: 100px;
        margin-bottom: 20px;
        background: rgba(248, 249, 251, 1);
        .part3-three-item-img {
          width: 46px;
          height: 44px;
        }
      }
      .part3-three-item-title {
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
      }
    }
  }
  .part3-four {
    width: 1180px;
    margin-bottom: 48px;
    margin-top: 60px;
    height: 465px;
    background: url("../../../../assets/imgs/pcpage3/p48.png") no-repeat center
      0 / cover;
  }
}

.part4 {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 72px;
  padding-bottom: 80px;
  background: rgba(248, 248, 248, 1);
  .text1 {
    margin-bottom: 14px;
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
  }
  .text2 {
    font-size: 18px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(136, 136, 136, 1);
    line-height: 32px;
    margin-bottom: 5px;
  }
  .loop {
    width: 1250px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 30px;
    .loop-item {
      margin-right: 66px;
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 50px;
      width: 350px;
      .loop-img {
        width: 120px;
        height: 120px;
      }
      .loop-title {
        margin-top: 32px;
        margin-bottom: 12px;
        font-size: 24px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(51, 51, 51, 1);
        line-height: 33px;
      }
      .loop-text {
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(102, 102, 102, 1);
        line-height: 30px;
      }
    }
  }
}

.part6 {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 72px;
  padding-bottom: 80px;
  .text1 {
    margin-bottom: 14px;
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
  }
  .part6-bg {
    position: relative;
    width: 1271px;
    height: 360px;
    background: url("../../../../assets/imgs/pcpage2/p10.png") no-repeat center
      0 / cover;
    margin-top: 60px;
    .part6-text {
      font-size: 16px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: rgba(85, 85, 85, 1);
      line-height: 30px;
      position: absolute;
      width: 336px;
      top: 52px;
    }
    .part6-text1 {
      left: 72px;
    }
    .part6-text2 {
      left: 472px;
    }
    .part6-text3 {
      left: 872px;
    }
  }
}
</style>