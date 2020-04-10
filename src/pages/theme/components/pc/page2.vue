<template>
  <div>
    <div class="post-bg">
      <span class="text2">[考研·留学·求职] 三选二</span>
      <span class="text3">用匠心成就大学生名校名企梦想</span>
      <div class="btn-text">定制你的计划</div>
    </div>

    <div class="part1">
      <span class="text1">为什么选择双轨计划</span>
      <span class="text2">大学生身处考研、留学、求职，三重困局，单一选择一条路径风险高</span>
      <div class="icon-line">
        <div v-for="item in part1Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <span class="text3">{{item.title}}</span>
          <span class="text4">{{item.text}}</span>
          <span class="text4">{{item.text1}}</span>
          <span class="text4">{{item.text2}}</span>
        </div>
      </div>
    </div>

    <div class="part2">
      <span class="text1">双轨计划核心理念</span>
      <span class="text2">以终为始,明确目标，就业/考研/出国，“三选二”</span>
      <div class="icon-line">
        <img src="@/assets/imgs/pcpage2/p2.png" class="icon" />
        <div class="right">
          <span class="text1">大学规划的核心是</span>
          <span class="text2">从大一开始明确目标，认清自身的优劣势，选好考研、留学、求职路径，协助青年构建底层通用胜任力，不断提升核心竞争力向目标前进，就能实现</span>
        </div>
      </div>
    </div>

    <div class="part3">
      <span class="text1">双轨计划优势</span>
      <div class="icon-line">
        <div v-for="item in part3Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <span class="text3">{{item.title}}</span>
          <div class="bottom-line"></div>
        </div>
      </div>
    </div>

    <div class="part4">
      <span class="text1">适宜4种人群</span>
      <div class="icon-line">
        <div v-for="item in part4Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <div class="middle-line"></div>
          <span class="text3">{{item.text}}</span>
        </div>
      </div>
    </div>

    <div class="part5">
      <span class="text1">可选双轨计划</span>
      <div class="icon-line">
        <div v-for="item in part5Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <span class="text3">{{item.title}}</span>
        </div>
      </div>
    </div>

    <div class="part6">
      <span class="text1">双轨培养体系</span>
      <span class="text2">兼顾学业与职业，以科学的方法、全新的视角，</span>
      <span class="text2">以终为始的规划考研，留学，求职三条路径，将时间及风险成本降到最低。</span>
      <div class="icon-line">
        <img src="@/assets/imgs/pcpage2/post.png" class="icon" />
      </div>
    </div>

    <div class="part7">
      <span class="text1">全能型人才核心竞争力模型</span>
      <span class="text2">大学生求职期间可以用“双轨制”进行全方位提升，尽早积累核心竞争力，成为全能型人才，</span>
      <span class="text2">便能轻松地在考研、留学、求职3条路上实现“3选2”， 在激烈的人才竞争中脱颖而出，实现职业理想。</span>
      <div class="icon-line">
        <img src="@/assets/imgs/pcpage2/p7.png" class="icon" />
        <div class="left">
          <span class="text3">全能型人才核心竞争力包含</span>
          <span class="text4">三个层次</span>
          <span class="text5">方向感知力、底层系统、胜任力。</span>
          <span class="text4">七个维度</span>
          <span class="text5">自我认知、目标研究、价值观、习惯、方法、通用胜任力、专项胜任力。</span>
        </div>
        <div class="right">
          <div v-for="item in part7Arr" :key="item.text" class="item">
            <img :src="item.img" class="icon2" />
            <span class="text6">{{item.text}}</span>
          </div>
          <div class="bottom">这些核心竞争力集于一身，便是全能型人才。</div>
        </div>
      </div>
    </div>

    <!-- ** -->
  </div>
</template>


<script>
const p11 = require("@/assets/imgs/pcpage2/p11.png");
const p12 = require("@/assets/imgs/pcpage2/p12.png");
const p13 = require("@/assets/imgs/pcpage2/p13.png");
const p31 = require("@/assets/imgs/pcpage2/p31.png");
const p32 = require("@/assets/imgs/pcpage2/p32.png");
const p33 = require("@/assets/imgs/pcpage2/p33.png");
const p34 = require("@/assets/imgs/pcpage2/p34.png");
const p35 = require("@/assets/imgs/pcpage2/p35.png");
const p42 = require("@/assets/imgs/pcpage2/p42.png");
const p43 = require("@/assets/imgs/pcpage2/p43.png");
const p44 = require("@/assets/imgs/pcpage2/p44.png");
const p45 = require("@/assets/imgs/pcpage2/p45.png");
const p51 = require("@/assets/imgs/pcpage2/p51.png");
const p52 = require("@/assets/imgs/pcpage2/p52.png");
const p53 = require("@/assets/imgs/pcpage2/p53.png");
const p54 = require("@/assets/imgs/pcpage2/p54.png");
const p71 = require("@/assets/imgs/pcpage2/p71.png");
const p72 = require("@/assets/imgs/pcpage2/p72.png");
const p73 = require("@/assets/imgs/pcpage2/p73.png");

export default {
  name: "page",
  data() {
    return {
      part1Arr: [
        {
          img: p11,
          title: "考研“难”",
          text: "2020考研报考人数突破300万大关",
          text1: "录取率降至17%",
          text2: "考研难上岸"
        },
        {
          img: p12,
          title: "留“假”学",
          text: "平均留学投入超过30万",
          text1: "45%留学生归国后月薪不超过6000",
          text2: "投入产出不成正比"
        },

        {
          img: p13,
          title: "“难”求职",
          text: "2019年的大学应届毕业生数量达834万",
          text1: "部分名企招聘量同比去年大幅下降51%",
          text2: "进名企越来越难"
        }
      ],
      part3Arr: [
        {
          title: "个性培养",
          text:
            "个性化目标设定，专属金牌教练全面跟踪，科学缜密的服务架构，多对一针对性精细化辅导",
          img: p31
        },
        {
          title: "专业师资",
          text:
            "考研、留学领域权威专项导师1V1咨询指导，各行业、企业、岗位的精英导师助力求职",
          img: p32
        },
        {
          title: "经验沉淀",
          text:
            "十余年教育领域实战经验及成果积累，用匠心,时刻坚守为金牌学徒的职业发展负责的初心",
          img: p33
        },
        {
          title: "多元选择",
          text:
            "以终为始，以就业为目标，提供多种服务组合，全面覆盖大学生需求点，助力未来发展",
          img: p34
        },
        {
          title: "结果保障",
          text:
            "包拿全职高薪工作，不达目标100%退还学费 高匹配度、高满意度的Offer成果，获得企业持续高度青睐",
          img: p35
        }
      ],
      part4Arr: [
        {
          text: "没有清晰的自我认知，没有明确目标的大一、大二学生",
          img: p42
        },
        {
          text: "有目标，但不知道怎样实现的大一、大二学生",
          img: p43
        },
        {
          text: "有考研想法，不想二战的大一、大二学生",
          img: p44
        },
        {
          text: "有点“贪心”，考研·留学·求职， 想走2条路径的大一、大二学生",
          img: p45
        }
      ],
      part5Arr: [
        { title: "考研+求职", img: p51 },
        { title: "考研+留学", img: p52 },
        { title: "留学+求职", img: p53 },
        { title: "考研·留学·求职 三选二", img: p54 }
      ],
      part7Arr: [
        { text: "职场精英具备什么样的核心竞争力?", img: p71 },
        { text: "考研学霸具备什么样的核心竞争力?", img: p72 },
        { text: "留学名校的学子具备什么样的核心竞争力?", img: p73 }
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
  background: url("../../../../assets/imgs/pcpage2/post.png") no-repeat center 0 /
    cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  .text2 {
    margin-top: 240px;
    font-size: 24px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
  }
  .text3 {
    margin-top: 20px;
    font-size: 28px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
  }
  .btn-text {
    cursor: pointer;
    margin-top: 46px;
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
  height: 563px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 72px 0 74px 0;
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
  }
  .text2 {
    margin-top: 14px;
    font-size: 18px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(136, 136, 136, 1);
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
      .icon {
        width: 100px;
        height: 100px;
      }
      .text3 {
        margin-top: 30px;
        font-size: 26px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(51, 51, 51, 1);
        margin-bottom: 10px;
      }
      .text4 {
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(136, 136, 136, 1);
        line-height: 28px;
      }
    }
  }
}

.part2 {
  background: rgba(248, 248, 248, 1);
  height: 780px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 72px;
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: 500;
    color: rgba(51, 51, 51, 1);
  }
  .text2 {
    margin-top: 14px;
    font-size: 18px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(136, 136, 136, 1);
  }
  .icon-line {
    display: flex;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon {
      width: 809px;
      height: 472px;
      margin-right: 10px;
    }
    .right {
      display: flex;
      flex-direction: column;
      .text1 {
        font-size: 28px;
        margin-top: 84px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(0, 0, 0, 1);
        margin-bottom: 30px;
      }
      .text2 {
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(102, 102, 102, 1);
        line-height: 36px;
      }
    }
  }
}

.part3 {
  height: 532px;
  display: flex;
  flex-direction: column;
  align-items: center;
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
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 220px;
      height: 270px;
      background: rgba(255, 255, 255, 1);
      box-shadow: 0px 2px 20px 0px rgba(204, 204, 204, 0.24);
      border-radius: 4px;
      .icon {
        width: 81px;
        height: 68px;
        margin-bottom: 25px;
      }
      .text3 {
        font-size: 22px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
      }
      .bottom-line {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 220px;
        height: 6px;
        background: linear-gradient(
          135deg,
          rgba(8, 85, 202, 1) 0%,
          rgba(8, 85, 202, 0.7) 100%
        );
        box-shadow: 0px 2px 18px 0px rgba(204, 204, 204, 0.31);
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
      }
    }
  }
}

.part4 {
  height: 554px;
  background: url("../../../../assets/imgs/pcpage2/p41.png") no-repeat center 0 /
    cover;
  display: flex;
  flex-direction: column;
  align-items: center;
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
      width: 280px;
      height: 292px;
      background: rgba(255, 255, 255, 1);
      box-shadow: 0px 2px 20px 0px rgba(204, 204, 204, 0.24);
      border-radius: 4px;
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

.part5 {
  height: 488px;
  display: flex;
  flex-direction: column;
  align-items: center;
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
      width: 280px;
      height: 226px;
      background: rgba(255, 255, 255, 1);
      box-shadow: 0px 4px 20px 0px rgba(0, 48, 120, 0.1);
      .icon {
        width: 81px;
        height: 68px;
        margin-bottom: 25px;
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

.part6 {
  height: 694px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 72px;
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
  }
  .icon-line {
    display: flex;
    align-items: center;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon {
      width: 1180px;
      height: 325px;
    }
  }
}

.part7 {
  height: 624px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 72px;
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
  }
  .icon-line {
    display: flex;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon {
      width: 48px;
      height: 41px; 
      margin-top: 31px;
    }
    .left {
      display: flex;
      flex-direction: column;
      .text3 {
        margin-top: 42px;
        font-size: 28px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
        margin-bottom: 16px;
      }
      .text4 {
        margin-top: 16px;
        margin-bottom: 14px;
        font-size: 22px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
      }
      .text5 {
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(102, 102, 102, 1);
      }
    }
    .right {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding-top: 44px;
      width: 560px;
      height: 284px;
      background: rgba(255, 255, 255, 1);
      box-shadow: 0px 2px 14px 0px rgba(204, 204, 204, 0.31);
      border: 1px solid rgba(8, 85, 202, 0.16);
      .item {
        display: flex;
        align-items: center;
        .icon2 {
          width: 30px;
          height: 30px;
          margin-left: 92px;
          margin-right: 12px;
        }
        .text6 {
          font-size: 18px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(51, 51, 51, 1);
        }
      }
      .bottom {
        height: 64px;
        background: linear-gradient(
          90deg,
          rgba(80, 134, 217, 1) 0%,
          rgba(10, 87, 203, 1) 100%
        );
        font-size: 24px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(255, 255, 255, 1);
        line-height: 64px;
        text-align: center;
      }
    }
  }
}
</style>