<template>
  <div>
    <div class="post-bg">
      <span class="text1">用匠心成就大学生名校名企梦想</span>
      <span class="text2">[考研·留学·求职] 三选二</span>
      <span class="text3">首推中国大学生学业职业“双轨计划”</span>
      <div class="btn-text">定制你的计划</div>
    </div>

    <div class="part1">
      <span class="text1">盈途影响力</span>
      <span class="text2">致力于通过“盈途双轨计划”，提供全面的学业、职业规划及成长方案，</span>
      <span class="text2">帮助中国青年学子建立自我认知，提升核心竞争力，最终实现名校名企梦想。</span>
      <div class="icon-line">
        <div v-for="item in part1Arr" :key="item.title" class="icon-item">
          <img :src="item.img" class="icon" />
          <span class="text3">{{item.title}}</span>
          <span class="text4">{{item.text}}</span>
        </div>
      </div>
    </div>

    <div class="part2">
      <span class="text1">盈途双轨计划</span>
      <span class="text2">为在校大学生构建全面的学业职业图景，以终为始，将职业目标与学业目标统一起来，进行学业职业双重规划，</span>
      <span class="text2">提前布局，两手准备，做好过程管理，个性化赋能，提升核心竞争力，实现学业职业理想。</span>
      <div class="icon-line">
        <div
          @mouseenter="p2Mouseenter($event,item.text)"
          @mouseleave="part2ActiveText=''"
          @click="()=>{part2ActiveText=item.text}"
          v-for="item in part2Arr"
          :key="item.text"
          :class="[
        'icon-item',
        part2ActiveText === item.text ?'part2-icon-item-active':''
        ]"
        >
          <img :src="part2ActiveText===item.text?item.imgc:item.img" class="icon" />
          <span
            class="text1"
            :style="{color:part2ActiveText===item.text?'rgba(255,255,255,1)':'rgba(51,51,51,1)'}"
          >{{item.text}}</span>
        </div>
      </div>
      <div class="btn-text">了解详情</div>
    </div>

    <div class="part3"></div>

    <img src="@/assets/imgs/pcpage1/p4.png" class="part4" />

    <div class="part5"></div>

    <div class="part6">
      <span class="text1">部分学徒OFFER展示</span>
      <div class="icon-line">
        <div
          @mouseenter="p6Mouseenter($event,item.title)"
          @mouseleave="part6ActiveText=''"
          @click="()=>{part6ActiveText=item.title}"
          :class="[
        'icon-item',
        part6ActiveText === item.title ?'part6-icon-item-active':''
        ]"
          v-for="item in part6Arr"
          :key="item.title"
          :style="{borderLeft:item.title==='留学OFFER'?'1px solid #d8d8d8':'',borderRight:item.title==='留学OFFER'?'1px solid #d8d8d8':''}"
        >
          <span>{{item.title}}</span>
        </div>
      </div>
      <img src="@/assets/imgs/pcpage1/p62.png" class="img" v-if="part6ActiveText==='考研OFFER'" />
      <img src="@/assets/imgs/pcpage1/p63.png" class="img" v-if="part6ActiveText==='留学OFFER'" />
      <img src="@/assets/imgs/pcpage1/p64.png" class="img" v-if="part6ActiveText==='求职OFFER'" />
    </div>

    <div class="part7"></div>

    <div class="part8">
      <span class="text1">盈途教育足迹</span>
      <div class="icon-line">
        <div
          @mouseenter="p8Mouseenter($event,item.title)"
          @mouseleave="part8ActiveTitle=''"
          @click="()=>{part8ActiveTitle=item.title}"
          :class="[
        'icon-item',
        part8ActiveTitle === item.title ?'part8-icon-item-active':''
        ]"
          v-for="item in part8Arr"
          :key="item.title"
        >
          <span
            class="f-B"
            :style="{ marginTop:'44px',fontSize:'32px',color:part8ActiveTitle === item.title?'white':'#0855CA'}"
          >{{item.title}}</span>
          <span :style="{ marginTop:'10px',fontSize:'14px'}">{{item.text1}}</span>
          <span :style="{ marginTop:'4px',fontSize:'14px'}">{{item.text2}}</span>
        </div>
      </div>
    </div>

    <div class="part9">
      <span class="text1">多家媒体报道</span>
      <div class="icon-line">
        <div class="icon-item" v-for="item in part9Arr" :key="item.title">
          <img :src="item" class="img" />
        </div>
      </div>
      <div class="btb-text">查看更多</div>
    </div>

    <div class="part10">
      <span class="text1">盈途动态</span>
      <div class="icon-line">
        <div class="icon-item" v-for="item in 4" :key="item.title">
          <img class="img" src="@/assets/imgs/pcpage1/p95.png" />
          <span class="text2 vertical-2">盈途教育获得数百万元战略投资共同布局新高考后生涯规划赛道涯规划赛道涯规划赛道</span>
        </div>
      </div>
    </div>
    <!-- ** -->
  </div>
</template>


<script>
const p11 = require("@/assets/imgs/pcpage1/p11.png");
const p12 = require("@/assets/imgs/pcpage1/p12.png");
const p13 = require("@/assets/imgs/pcpage1/p13.png");
const p14 = require("@/assets/imgs/pcpage1/p14.png");
const p15 = require("@/assets/imgs/pcpage1/p15.png");
const p21c = require("@/assets/imgs/pcpage1/p21c.png");
const p21 = require("@/assets/imgs/pcpage1/p21.png");
const p22c = require("@/assets/imgs/pcpage1/p22c.png");
const p22 = require("@/assets/imgs/pcpage1/p22.png");
const p23c = require("@/assets/imgs/pcpage1/p23c.png");
const p23 = require("@/assets/imgs/pcpage1/p23.png");
const p4 = require("@/assets/imgs/pcpage1/p4.png");
const p91 = require("@/assets/imgs/pcpage1/p91.png");
const p92 = require("@/assets/imgs/pcpage1/p92.png");
const p93 = require("@/assets/imgs/pcpage1/p93.png");
const p94 = require("@/assets/imgs/pcpage1/p94.png");
const p95 = require("@/assets/imgs/pcpage1/p95.png");

export default {
  name: "page",
  data() {
    return {
      part1Arr: [
        { img: p11, title: "10年+", text: "考研·留学·求职经验" },
        {
          img: p12,
          title: "5000+",
          text: "学员验证"
        },
        {
          img: p13,
          title: "4.2个/人",
          text: "2019年学徒人均斩获名校名企offer"
        },
        { img: p14, title: "品牌背书", text: "获得上市公司立思辰天使投资" },
        { img: p15, title: "1000+", text: "行业导师传授经验" }
      ],
      part2Arr: [
        { img: p21, imgc: p21c, text: "考研+求职" },
        { img: p22, imgc: p22c, text: "考研+留学" },
        { img: p23, imgc: p23c, text: "留学+求职" }
      ],
      part2ActiveText: "考研+求职",
      part6Arr: [
        { title: "考研OFFER" },
        { title: "留学OFFER" },
        { title: "求职OFFER" }
      ],
      part6ActiveText: "考研OFFER",
      part8Arr: [
        { title: "150+", text1: "2019年全国大学生", text2: "生涯规划讲座" },
        { title: "30+", text1: "2019年全国讲座", text2: "覆盖城市" },
        { title: "10+", text1: "2019年受邀走进的", text2: "大学" }
      ],
      part8ActiveTitle: "150+",
      part9Arr: [p91, p92, p93, p94, p95]
    };
  },
  props: {},
  components: {},
  mounted() {},
  created() {},
  computed: {},
  watch: {},
  methods: {
    p2Mouseenter(e, text) {
      this.part2ActiveText = text;
    },
    p6Mouseenter(e, title) {
      this.part6ActiveText = title;
    },
    p8Mouseenter(e, title) {
      this.part8ActiveTitle = title;
    }
  }
};
</script>
<style lang="scss" scoped>
.post-bg {
  height: 960px;
  width: 100%;
  background: url("../../../../assets/imgs/pcpage1/post.png") no-repeat center 0 /
    cover;
  margin-top: -90px;
  display: flex;
  flex-direction: column;
  align-items: center;
  .text1 {
    font-size: 66px;
    font-family: PingFangSC-Semibold, PingFang SC;
    font-weight: 600;
    color: rgba(255, 255, 255, 1);
    margin-top: 241px;
  }
  .text2 {
    font-size: 30px;
    font-family: PingFangSC-Semibold, PingFang SC;
    font-weight: 600;
    color: rgba(255, 255, 255, 1);
    margin-top: 90px;
  }
  .text3 {
    font-size: 36px;
    font-family: PingFangSC-Semibold, PingFang SC;
    font-weight: 600;
    color: rgba(255, 255, 255, 1);
    margin-top: 40px;
  }
  .btn-text {
    width: 200px;
    height: 52px;
    background: rgba(255, 153, 6, 1);
    border-radius: 28px;
    font-size: 20px;
    font-family: PingFangSC-Semibold, PingFang SC;
    font-weight: 600;
    color: rgba(255, 255, 255, 1);
    line-height: 52px;
    text-align: center;
    margin-top: 87px;
  }
}

.part1 {
  height: 520px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 72px 0 78px 0;
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: bold;
    color: rgba(51, 51, 51, 1);
  }
  .text2 {
    margin-top: 16px;
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
        margin-top: 20px;
        font-size: 24px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: bold;
        color: rgba(51, 51, 51, 1);
      }
      .text4 {
        margin-top: 10px;
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(102, 102, 102, 1);
      }
    }
  }
}

.part2 {
  height: 676px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 72px 0 78px 0;
  background: rgba(248, 248, 248, 1);
  .text1 {
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: bold;
    color: rgba(51, 51, 51, 1);
  }
  .text2 {
    margin-top: 16px;
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
      cursor: pointer;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 376px;
      height: 248px;
      background: rgba(255, 255, 255, 1);
      box-shadow: 0px 2px 14px 0px rgba(204, 204, 204, 0.3);
      border-radius: 6px;
      .icon {
        width: 50px;
        height: 50px;
        margin-bottom: 40px;
      }
      .text1 {
        font-size: 20px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
      }
    }
  }
  .btn-text {
    width: 240px;
    height: 48px;
    background: rgba(255, 153, 6, 1);
    box-shadow: 0px 2px 10px 0px rgba(255, 153, 6, 0.4);
    border-radius: 24px;
    font-size: 20px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
    line-height: 48px;
    text-align: center;
    margin-top: 50px;
  }
}
.part2-icon-item-active {
  background: #0855ca !important;
}

.part3 {
  height: 830px;
  border: 1px solid red;
}

.part4 {
  width: 100%;
  height: 740px;
}

.part5 {
  height: 710px;
  border: 1px solid red;
}

.part6 {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 717px;
  background: url("../../../../assets/imgs/pcpage1/p61.png") no-repeat center 0 /
    cover;
  .text1 {
    margin-top: 72px;
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: bold;
    color: rgba(51, 51, 51, 1);
  }
  .icon-line {
    display: flex;
    border: 1px solid #d8d8d8;
    margin-top: 60px;
    .icon-item {
      width: 150px;
      height: 55px;
      font-size: 20px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      line-height: 50px;
      text-align: center;
      background: white;
      color: rgba(102, 102, 102, 1);
      cursor: pointer;
    }
  }
  .img {
    width: 1180px;
    height: 360px;
    margin-top: 40px;
  }
}
.part6-icon-item-active {
  background: rgba(8, 85, 202, 1) !important;
  border: 1px solid rgba(8, 85, 202, 1) !important;
  color: white !important;
}

.part7 {
  height: 728px;
  border: 1px solid red;
}

.part8 {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 600px;
  background: url("../../../../assets/imgs/pcpage1/p81.png") no-repeat center 0 /
    cover;
  .text1 {
    margin-top: 83px;
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: bold;
    color: rgba(51, 51, 51, 1);
  }
  .icon-line {
    display: flex;
    margin-top: 81px;
    width: 1180px;
    justify-content: space-between;
    .icon-item {
      cursor: pointer;
      width: 220px;
      height: 220px;
      border-radius: 110px;
      border: 1px dotted rgba(153, 153, 153, 1);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-items: center;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
    }
  }
}
.part8-icon-item-active {
  background: rgba(8, 85, 202, 1) !important;
  color: white !important;
}

.part9 {
  height: 482px;
  display: flex;
  flex-direction: column;
  align-items: center;
  .text1 {
    margin-top: 72px;
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: bold;
    color: rgba(51, 51, 51, 1);
  }
  .icon-line {
    display: flex;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon-item {
      .img {
        width: 220px;
        height: 132px;
        background: rgba(255, 255, 255, 1);
        border-radius: 4px;
        border: 1px solid rgba(216, 216, 216, 1);
      }
    }
  }
  .btb-text {
    width: 240px;
    height: 48px;
    background: rgba(255, 153, 6, 1);
    box-shadow: 0px 2px 10px 0px rgba(255, 153, 6, 0.4);
    border-radius: 24px;
    font-size: 20px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(255, 255, 255, 1);
    line-height: 48px;
    text-align: center;
    margin-top: 50px;
  }
}

.part10 {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 498px;
  background: rgba(248, 248, 248, 1);
  // background-size:936px 448px;
  // background: url("../../../../assets/imgs/pcpage1/p101.png") no-repeat center 0 /
  // cover;
  .text1 {
    margin-top: 72px;
    font-size: 36px;
    font-family: PingFangSC-Medium, PingFang SC;
    font-weight: bold;
    color: rgba(51, 51, 51, 1);
  }
  .icon-line {
    display: flex;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-items: center;
      .img {
        width: 280px;
        height: 171px;
      }
      .text2 {
        font-size: 16px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(51, 51, 51, 1);
        line-height: 28px;
        width: 280px;
        margin-top: 14px;
      }
    }
  }
}
</style>