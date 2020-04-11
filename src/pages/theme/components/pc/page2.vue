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
        <div
          v-for="item in part3Arr"
          :key="item.title"
          class="icon-item"
          @mouseenter="p3Mouseenter($event,item.title)"
          @mouseleave="part3ActiveTitle=''"
        >
          <div class="icon-fake-bg" v-if="part3ActiveTitle===item.title">
            <span class="icon-fake-bg-text1">{{item.title}}</span>
            <div class="icon-fake-bg-line"></div>
            <span class="icon-fake-bg-text2">{{item.text}}</span>
          </div>

          <img :src="item.img" class="icon" v-if="part3ActiveTitle!==item.title"/>
          <span class="text3" v-if="part3ActiveTitle!==item.title">{{item.title}}</span>
          <div class="bottom-line" v-if="part3ActiveTitle!==item.title"></div>
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

    <div class="part8">
      <span class="text1">双轨服务内容</span>
      <span class="text2">13大通用能力，[考研·留学·求职] 三选二，双轨路径培养，</span>
      <span class="text2">科学规划，提前布局，应势利异，个性化赋能，让你的大学拼的稳妥，赢得从容！</span>

      <div class="title">
        <div class="title-line"></div>
        <span class="title-text">
          13大底层通用能力培养
          <br />构建大学生核心通用胜任力
        </span>
        <div class="title-line"></div>
      </div>
      <div class="one">
        <div
          v-for="(item,index) in part8Arr_one"
          :key="item.title"
          :class="[
          'item-one',
          index<4?'h500':'h436'
          ] "
        >
          <div class="item-one-top">
            <img :src="item.img" class="item-one-top-img" />
            <span class="item-one-top-title">{{item.title}}</span>
            <span class="item-one-top-text">{{item.text}}</span>
          </div>
          <div class="item-one-bottom-all">
            <div class="item-one-bottom" v-for="item in item.loop" :key="item">
              <div class="item-one-bottom-radius"></div>
              <span class="item-one-bottom-text">{{item}}</span>
            </div>
          </div>
        </div>
        <div class="one-bottom">
          <div class="one-bottom-line1">
            <span class="one-bottom-line1-text">英语训练</span>
            <div class="one-bottom-line1-img">赠送</div>
          </div>
          <span class="one-bottom-line1-text1">
            听说读写四个维度全方位提高
            <br />学徒英语语言能力运用及应试水平
          </span>
          <div class="one-bottom-line3">
            <div class="one-bottom-line3-radius"></div>
            <span class="one-bottom-line3-text">英语各阶段学习目标及计划制定</span>
            <div class="one-bottom-line3-radius"></div>
            <span class="one-bottom-line3-text">基础方法论课程</span>
            <div class="one-bottom-line3-radius"></div>
            <span class="one-bottom-line3-text">大学四六级课程</span>
            <div class="one-bottom-line3-radius"></div>
            <span class="one-bottom-line3-text">留学标化考试课程</span>
          </div>
        </div>
      </div>

      <div class="title">
        <div class="title-line"></div>
        <span class="title-text">
          双轨路径培养
          <br />[考研·留学·求职] 三选二
        </span>
        <div class="title-line"></div>
      </div>

      <div class="two">
        <div v-for="item in part8Arr_two" :key="item.title" class="item-two">
          <div class="item-two-top">
            <img :src="item.img" class="item-two-top-img" />
            <span class="item-two-top-title">{{item.title}}</span>
            <span class="item-two-top-text">{{item.text}}</span>
          </div>
          <div class="item-two-bottom-all">
            <div class="item-two-bottom" v-for="item in item.loop" :key="item">
              <div class="item-two-bottom-radius"></div>
              <span class="item-two-bottom-text">{{item}}</span>
            </div>
          </div>
        </div>
      </div>

      <div class="title">
        <div class="title-line"></div>
        <span class="title-text">OFFER达成</span>
        <div class="title-line"></div>
      </div>

      <div class="three">
        <div class="three-item" v-for="item in part8Arr_three" :key="item.text">
          <img :src="item.img" class="three-item-img" />
          <span class="three-item-text">{{item.text}}</span>
        </div>
      </div>
    </div>

    <div class="part9">
      <span class="text1">多对一专属服务</span>
      <span class="text2">用匠心，守初心，成就学徒名校名企梦想</span>
      <div class="loop">
        <div class="loop-item" v-for="item in part9Arr" :key="item.title">
          <img :src="item.img" class="loop-img" />
          <span class="loop-title">{{item.title}}</span>
          <span class="loop-text">{{item.text}}</span>
        </div>
      </div>
    </div>

    <div class="part10">
      <span class="text1">学徒好评</span>
      <div class="part10-bg">
        <span
          class="part10-text part10-text1"
        >在选择盈途教育双轨计划的时候，其实我曾经是一度有怀疑的，但是我不想错失老师们说的双条路径规划的机会，所以我抱着试试看的心态进入了进来。进来之后老师们对我目标的设定、对我的阶段的培养、对我每个阶段的监督和帮助，是我没想到的。我从怀疑到感激再到后悔加入的太晚，如果你目前也在观望是否要加入盈途双轨计划，我建议你一定要进来，你将收获不一样的世界观。</span>
        <span
          class="part10-text part10-text2"
        >盈途是我见过的最有情怀的大学生教育机构。我见过其他培训机构都是以盈利为重，忽视学员的教学质量。在盈途，老师都是二十四小时在线，学员的问题都会得到及时地答复，一点不耽误学习进程。全身心投入付出，只为给大家带来更好的陪伴式学习的服务体验，感谢每一位老师的付出，在过程中不断的鼓励我、支持我、陪伴我，协助我拿到了我理想的OFFER。</span>
        <span
          class="part10-text part10-text3"
        >通过盈途双轨计划，让我学到了很多课本上学不到的东西，让我开始走出大学校园这样一个象牙塔，开始真正接触到社会，接触到真实的人和事。在大学期间，一定要利用好空闲的时间，去了解各行各业、各个职业是什么样子的。在这个过程中，非常幸运有盈途的老师们一直带着我，让我了解到了金融、快消还有互联网的公司，原来真的和我想象中非常不同，我才更清晰的了解自己的职业目标，走好自己的学业道理。</span>
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
const p8_11 = require("@/assets/imgs/pcpage2/p8_11.png");
const p8_12 = require("@/assets/imgs/pcpage2/p8_12.png");
const p8_13 = require("@/assets/imgs/pcpage2/p8_13.png");
const p8_14 = require("@/assets/imgs/pcpage2/p8_14.png");
const p8_15 = require("@/assets/imgs/pcpage2/p8_15.png");
const p8_16 = require("@/assets/imgs/pcpage2/p8_16.png");
const p8_17 = require("@/assets/imgs/pcpage2/p8_17.png");
const p8_18 = require("@/assets/imgs/pcpage2/p8_18.png");
const p8_19 = require("@/assets/imgs/pcpage2/p8_19.png");
const p8_20 = require("@/assets/imgs/pcpage2/p8_20.png");
const p8_21 = require("@/assets/imgs/pcpage2/p8_21.png");
const p8_22 = require("@/assets/imgs/pcpage2/p8_22.png");
const p8_23 = require("@/assets/imgs/pcpage2/p8_23.png");
const p8_25 = require("@/assets/imgs/pcpage2/p8_25.png");
const p8_26 = require("@/assets/imgs/pcpage2/p8_26.png");
const p8_27 = require("@/assets/imgs/pcpage2/p8_27.png");
const p8_28 = require("@/assets/imgs/pcpage2/p8_28.png");
const p8_29 = require("@/assets/imgs/pcpage2/p8_29.png");
const p8_30 = require("@/assets/imgs/pcpage2/p8_30.png");
const p91 = require("@/assets/imgs/pcpage2/p91.png");
const p92 = require("@/assets/imgs/pcpage2/p92.png");
const p93 = require("@/assets/imgs/pcpage2/p93.png");
const p94 = require("@/assets/imgs/pcpage2/p94.png");
const p95 = require("@/assets/imgs/pcpage2/p95.png");
const p96 = require("@/assets/imgs/pcpage2/p96.png");

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
      part3ActiveTitle: "",
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
      ],
      part8Arr_one: [
        {
          img: p8_11,
          title: "评估中心",
          text: "专业测评老师定期出具学徒个人竞争力及阶段性成长报告",
          loop: ["个人竞争力评估", "阶段性成长报告", "模块评估反馈"]
        },
        {
          img: p8_12,
          title: "成长指导",
          text:
            "成长导师，服务教练，模块老师，路径专家全方位支持学徒个人发展与成长",
          loop: [
            "学徒档案建立",
            "课业规划及管理",
            "路径规划",
            "性格测评及优劣势挖掘",
            "职业规划",
            "自我认知分析",
            "阶段性培养计划"
          ]
        },
        {
          img: p8_13,
          title: "底层系统",
          text:
            "构建正确的信念及价值观，学会思考并形成习惯，持续输出正确的行为",
          loop: ["思维力训练", "商业思维入门", "习惯养成"]
        },
        {
          img: p8_14,
          title: "校园生活(大一、大二适用)",
          text: "教练，导师全程跟踪学徒在校发展，助力未来路径目标达成",
          loop: [
            "入学指导",
            "课外活动甄选与建议",
            "社团竞选及留任辅导",
            "专业资质考试选择指导"
          ]
        },
        {
          img: p8_15,
          title: "背景提升",
          text: "制定背景（经历）提升方案，强化硬件",
          loop: ["商业竞赛经验分享与指导", "交流交换项目申请及建议(单独付费)"]
        },
        {
          img: p8_16,
          title: "阅读计划",
          text: "培养学徒阅读习惯，提升综合素养，丰富底蕴积累",
          loop: [
            "阅读习惯养成",
            "行业职业精选书单",
            "学期读书计划",
            "阅读方法与技巧"
          ]
        },
        {
          img: p8_17,
          title: "行业认知",
          text:
            "培养学徒行业认知的能力，能够快速整合并汇总信息，掌握基础分析技能",
          loop: [
            "热门行业概况课程",
            "十大行业核心业务解析",
            "行业认知技能与技巧掌握",
            "专业报告拆分解读",
            "个性化行业报告撰写制作"
          ]
        },
        {
          img: p8_18,
          title: "实习实践",
          text:
            "结合学徒未来路径方向，针对性提供行业，企业的实习项目，并协助学徒申请全职实习机会",
          loop: [
            "远程在线实习项目（PTA）",
            "进阶名企实习",
            "全职推优实习",
            "CDC实习信息汇总与推送",
            "实习过程管理及复盘总结"
          ]
        },
        {
          img: p8_19,
          title: "胜任力",
          text:
            "根据路径、行业及企业的能力要求针对性培养学徒的个人竞争力和综合素养",
          loop: [
            "通用行业技巧培养",
            "综合素养提升",
            "职场管理与沟通",
            "项目管理与时间管理"
          ]
        },
        {
          img: p8_20,
          title: "简历文书",
          text: "指导协助学徒完成各路径所需的中英基础文书材料准备",
          loop: [
            "中英文简历制作",
            "求职信息搜集与申请指导",
            "OQ解析",
            "求职信、感谢信撰写"
          ]
        },
        {
          img: p8_21,
          title: "笔试训练",
          text:
            "根据历年企业招聘及考研院校要求，提供针对性的学习课程及答疑指导",
          loop: [
            "笔试综合能力评估",
            "通用笔试技能讲解及训练",
            "行业企业笔试真题解析及辅导"
          ]
        },
        {
          img: p8_22,
          title: "面试表达",
          text: "强化学徒面试能力， 并量身打造面试回答",
          loop: [
            "个性化面试素材梳理",
            "自我介绍打磨",
            "中英文单面解析与模拟",
            "群面案例剖析及技巧讲解",
            "线上、线下面试训练与指导"
          ]
        }
      ],
      part8Arr_two: [
        {
          img: p8_25,
          title: "考研",
          text: "考研全过程精细化管理，助力学徒考取理想院校",
          loop: [
            "考研规划与指导",
            "考研目标院校分历年招录分析",
            "考研目标院校选择及策略制定",
            "备考计划与进度监控",
            "考研基础公共课程",
            "公共课程辅导与答疑",
            "心态调整与情绪管理",
            "考研报名流程解析与指导",
            "复试面试指导（非专业部分）",
            "研究生入学指导与建议"
          ]
        },
        {
          img: p8_26,
          title: "留学",
          text: "留学各环节深度参与，最大化学徒留学院校申请结果",
          loop: [
            "留学规划与指导",
            "目标院校历年招录情报对比",
            "目标院校选择及标化要求确定",
            "留学文书撰写与修改",
            "申请材料收集及信息审阅",
            "提交院校申请",
            "留学面试指导（非专业部分）",
            "留学OFFER竞争力分析及选择建议",
            "留学签证办理",
            "留学国家餐饮住宿技巧与建议"
          ]
        },
        {
          img: p8_27,
          title: "求职",
          text: "校招过程中步步为营，以终为始保障实现学徒职业目标",
          loop: [
            "职业兴趣与能力评估及规划",
            "历年校招招录比分析",
            "校招流程解析及笔面试策略",
            "行业技能技巧巩固加强",
            "校招文书个性化修改",
            "历年校招笔面试真题解析",
            "校招信息汇总与推送",
            "目标行业导师1V1指导面试",
            "求职OFFER竞争力分析及选择建议",
            "校招签约谈判指导与建议"
          ]
        }
      ],
      part8Arr_three: [
        { img: p8_28, text: "OFFER选择建议" },
        { img: p8_29, text: "职业保年薪" },
        { img: p8_30, text: "学业保排名" }
      ],
      part9Arr: [
        {
          title: "生涯规划专家",
          text:
            "拥有10年以上大学生学业、就业规划发展指导经验，熟悉学业及就业特点，指导学徒通过专业测评工具自我发现，引导规划及调整学业及职业方向，制定各阶段提升策略，解决学业及职业中方向性及关键性问题。",
          img: p91
        },
        {
          title: "学业职业导师",
          text:
            "拥有10年以上大学生学业、职业单项指导经验，发掘学徒的优势，根据学徒的求职、留学、考研的不同需求，制定各阶段的提升策略，解决其在学业、就业过程中的关键问题。",
          img: p92
        },
        {
          title: "资深授课老师",
          text:
            "拥有5年以上相关课程的授课经验，用浅显易懂的语言、本着以学生为主体的教学理念，注重调动和激发学生的自主性，帮助学生提升学业或就业技能。",
          img: p93
        },
        {
          title: "优秀行业导师",
          text:
            "超过1000名已毕业的优秀学徒自愿加入双轨计划成为兼职行业导师。他们理解求职痛点，更懂培养规则，将感恩化作有效反哺行动，用工作经验、机会推荐和一手信息等带领后辈成长。",
          img: p94
        },
        {
          title: "名企精英导师",
          text:
            "导师来自汇丰、渣打、摩立特、BCG、普华、德勤、宝洁、玛氏、百度、腾讯、阿里等主流行业里的明星企业，将名企求职与工作经历细化分解后传递给学徒，让学徒深度理解行业背景下企业的各种细节，使职业能力提升更具针对性。",
          img: p95
        },
        {
          title: "成长陪伴教练",
          text:
            "1V1全程学徒服务跟踪，具备超强的亲和力、责任心及洞察力，全面负责学徒建档、追踪、提升计划制定及监控，全程辅导学业、就业过程，协调各领域导师、专业团队及资源帮助学徒达成目标。",
          img: p96
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
  methods: {
    p3Mouseenter(e, title) {
      this.part3ActiveTitle = title;
    }
  }
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
    position: relative;
    display: flex;
    align-items: center;
    margin-top: 60px;
    width: 1180px;
    justify-content: space-between;
    .icon-fake-bg {
      position: absolute;
      top: 0;
      left: 0;
      width: 220px;
      height: 270px;
      background: linear-gradient(
        135deg,
        rgba(8, 85, 202, 1) 0%,
        rgba(8, 85, 202, 0.7) 100%
      );
      box-shadow: 0px 2px 20px 0px rgba(204, 204, 204, 0.24);
      border-radius: 4px;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 0 32px;
      .icon-fake-bg-text1 {
        margin-top: 44px;
        font-size: 22px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(255, 255, 255, 1);
        line-height: 30px;
      }
      .icon-fake-bg-line {
        margin-top: 14px;
        margin-bottom: 20px;
        width: 34px;
        height: 3px;
        background: rgba(255, 255, 255, 1);
        border-radius: 2px;
      }
      .icon-fake-bg-text2 {
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(255, 255, 255, 1);
        line-height: 26px;
      }
    }
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

.part8 {
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
  }
  .one {
    display: flex;
    justify-content: space-between;
    width: 1180px;
    flex-wrap: wrap;
    .item-one {
      width: 280px;
      background: rgba(248, 248, 248, 1);
      border: 1px solid rgba(151, 151, 151, 1);
      margin-bottom: 20px;
      .item-one-top {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 280px;
        height: 228px;
        background: rgba(3, 55, 134, 0.06);
        padding: 35px 16px 30px 16px;
        line-height: 32px;
        .item-one-top-img {
          width: 50px;
          height: 50px;
        }
        .item-one-top-title {
          font-size: 20px;
          margin-top: 20px;
          margin-bottom: 8px;
          font-family: PingFangSC-Medium, PingFang SC;
          font-weight: 500;
          color: rgba(51, 51, 51, 1);
        }
        .item-one-top-text {
          font-size: 14px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(136, 136, 136, 1);
          line-height: 26px;
          text-align: center;
        }
      }
      .item-one-bottom-all {
        padding-top: 24px;
        .item-one-bottom {
          padding-left: 20px;
          display: flex;
          align-items: center;
          .item-one-bottom-radius {
            width: 4px;
            height: 4px;
            background: rgba(8, 85, 202, 1);
            opacity: 0.4986;
            margin-right: 8px;
          }
          .item-one-bottom-text {
            font-size: 16px;
            font-family: PingFangSC-Regular, PingFang SC;
            font-weight: 400;
            color: rgba(119, 119, 119, 1);
            line-height: 32px;
          }
        }
      }
    }
    .one-bottom {
      display: flex;
      flex-direction: column;
      margin-bottom: 32px;
      width: 1180px;
      height: 180px;
      background: url("../../../../assets/imgs/pcpage2/p8_23.png") no-repeat
        center 0 / cover;
      padding-left: 124px;
      .one-bottom-line1 {
        display: flex;
        align-items: center;
        padding-top: 30px;
        margin-bottom: 12px;
        .one-bottom-line1-text {
          font-size: 26px;
          font-family: PingFangSC-Medium, PingFang SC;
          font-weight: 500;
          color: rgba(51, 51, 51, 1);
          line-height: 32px;
        }
        .one-bottom-line1-img {
          margin-left: 8px;
          padding-left: 5px;
          width: 57px;
          height: 26px;
          text-align: center;
          line-height: 26px;
          background: url("../../../../assets/imgs/pcpage2/p8_24.png") no-repeat
            center 0 / cover;
          font-size: 18px;
          font-family: PingFangSC-Medium, PingFang SC;
          font-weight: 500;
          color: rgba(248, 248, 248, 1);
          text-align: center;
        }
      }
      .one-bottom-line1-text1 {
        font-size: 14px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(85, 85, 85, 1);
        line-height: 22px;
      }
      .one-bottom-line3 {
        display: flex;
        align-items: center;
        padding-top: 12px;
        margin-bottom: 12px;
        .one-bottom-line3-radius {
          width: 4px;
          height: 4px;
          background: rgba(8, 85, 202, 1);
          opacity: 0.4986;
          margin-right: 8px;
        }
        .one-bottom-line3-text {
          font-size: 14px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(119, 119, 119, 1);
          line-height: 32px;
          margin-right: 40px;
        }
      }
    }
  }
  .two {
    display: flex;
    justify-content: space-between;
    width: 1180px;
    flex-wrap: wrap;
    .item-two {
      width: 380px;
      height: 570px;
      background: rgba(248, 248, 248, 1);
      border: 1px solid rgba(151, 151, 151, 1);
      margin-bottom: 20px;
      .item-two-top {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        width: 380px;
        height: 202px;
        background: rgba(3, 55, 134, 0.06);
        padding: 35px 22px 30px 22px;
        .item-two-top-img {
          width: 50px;
          height: 50px;
        }
        .item-two-top-title {
          font-size: 20px;
          font-family: PingFangSC-Medium, PingFang SC;
          font-weight: 500;
          color: rgba(51, 51, 51, 1);
        }
        .item-two-top-text {
          font-size: 14px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: rgba(136, 136, 136, 1);
          line-height: 26px;
          text-align: center;
        }
      }
      .item-two-bottom-all {
        padding-top: 24px;
        .item-two-bottom {
          display: flex;
          align-items: center;
          padding-left: 20px;
          .item-two-bottom-radius {
            width: 4px;
            height: 4px;
            background: rgba(8, 85, 202, 1);
            opacity: 0.4986;
            margin-right: 8px;
          }
          .item-two-bottom-text {
            font-size: 16px;
            font-family: PingFangSC-Regular, PingFang SC;
            font-weight: 400;
            color: rgba(119, 119, 119, 1);
            line-height: 32px;
          }
        }
      }
    }
  }
  .three {
    display: flex;
    justify-content: space-between;
    width: 1180px;
    .three-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 380px;
      height: 220px;
      background: rgba(248, 248, 248, 1);
      border: 1px solid rgba(151, 151, 151, 1);
      .three-item-img {
        width: 50px;
        height: 50ox;
        margin-bottom: 24px;
      }
      .three-item-text {
        font-size: 20px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(51, 51, 51, 1);
      }
    }
  }
  .title {
    margin-top: 40px;
    display: flex;
    align-items: center;
    margin-bottom: 60px;
    .title-text {
      font-size: 24px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: rgba(51, 51, 51, 1);
      line-height: 40px;
      text-align: center;
      margin: 0 30px;
    }
    .title-line {
      width: 220px;
      height: 1px;
      background-color: #333333;
    }
  }
}

.part9 {
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
  .text2 {
    font-size: 18px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(136, 136, 136, 1);
    line-height: 32px;
    margin-bottom: 5px;
  }
  .loop {
    width: 1180px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .loop-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 37px;
      width: 350px;
      .loop-img {
        width: 150px;
        height: 150px;
      }
      .loop-title {
        font-size: 24px;
        font-family: PingFangSC-Medium, PingFang SC;
        font-weight: 500;
        color: rgba(51, 51, 51, 1);
        line-height: 33px;
        margin: 20px 0 12px 0;
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

.part10 {
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
  .part10-bg {
    position: relative;
    width: 1271px;
    height: 360px;
    background: url("../../../../assets/imgs/pcpage2/p10.png") no-repeat center
      0 / cover;
    margin-top: 60px;
    .part10-text {
      font-size: 16px;
      font-family: PingFangSC-Regular, PingFang SC;
      font-weight: 400;
      color: rgba(85, 85, 85, 1);
      line-height: 30px;
      position: absolute;
      width: 336px;
      top: 52px;
    }
    .part10-text1 {
      left: 72px;
    }
    .part10-text2 {
      left: 472px;
    }
    .part10-text3 {
      left: 872px;
    }
  }
}
.h500 {
  height: 500px;
}
.h436 {
  height: 436px;
}
</style>