<template>
  <div class=".container">
    <el-container>
      <el-header>
        <el-menu :default-active="activeIndex2"
                 class="el-menu-demo"
                 mode="horizontal"
                 @select="handleSelect"
                 background-color="#545c64"
                 text-color="#fff"
                 active-text-color="#ffd04b">
          <el-menu-item index="1">POP管理</el-menu-item>
          <el-menu-item index="2">拍摄图库</el-menu-item>
          <el-menu-item index="3">设计模板</el-menu-item>
          <el-menu-item index="4">灵感库</el-menu-item>
          <el-menu-item index="5">共享文件</el-menu-item>
          <el-menu-item index="6">推广素材</el-menu-item>
          <el-menu-item index="7">视频素材</el-menu-item>
        </el-menu>
      </el-header>
      <el-main>
        <div class="main-nav">
          <div class="main-nav-first">
            <div>
              <div class="main-nav-result">共<span>23334</span>个结果</div>
              <div class="main-nav-radio">
                <el-radio v-model="radio"
                          label="1">货物</el-radio>
                <el-radio v-model="radio"
                          label="2">标签</el-radio>
                <el-radio v-model="radio"
                          label="3">备注</el-radio>
              </div>
              <div class="man-nav-input">
                <el-input placeholder="请输入内容"
                          v-model="input"
                          clearable>
                  <i slot="suffix"
                     class="el-input__icon el-icon-search"></i>
                </el-input>
              </div>
            </div>
          </div>
          <div class="main-nav-second">
            <el-tabs v-model="activeName"
                     @tab-click="handleClick">
              <el-tab-pane label="品牌"
                           name="first">
                <el-row>
                  <el-button round
                             size="mini">安踏anta</el-button>
                  <el-button round
                             size="mini">李宁</el-button>
                  <el-button round
                             size="mini">乔丹</el-button>
                  <el-button round
                             size="mini">耐克</el-button>
                  <el-button round
                             size="mini">阿迪达斯</el-button>
                </el-row>
              </el-tab-pane>
              <el-tab-pane label="年份"
                           name="second">
                <el-row>
                  <el-button round
                             size="mini">2019</el-button>
                  <el-button round
                             size="mini">2018</el-button>
                  <el-button round
                             size="mini">2017</el-button>
                  <el-button round
                             size="mini">2016</el-button>
                  <el-button round
                             size="mini">2015</el-button>
                  <el-button round
                             size="mini">2014</el-button>
                </el-row>
              </el-tab-pane>
              <el-tab-pane label="类目"
                           name="third">
                <el-row>
                  <el-button round
                             size="mini">男鞋</el-button>
                  <el-button round
                             size="mini">女鞋</el-button>
                  <el-button round
                             size="mini">运动鞋</el-button>
                  <el-button round
                             size="mini">双肩包</el-button>
                  <el-button round
                             size="mini">拉杆箱</el-button>
                  <el-button round
                             size="mini">男装</el-button>
                  <el-button round
                             size="mini">女装</el-button>
                  <el-button round
                             size="mini">童装</el-button>
                  <el-button round
                             size="mini">腕表/珠宝配饰/眼镜</el-button>
                  <el-button round
                             size="mini">童鞋</el-button>
                  <el-button round
                             size="mini">电器</el-button>
                  <el-button round
                             size="mini">母婴用品</el-button>
                </el-row>
              </el-tab-pane>
              <el-tab-pane label="端口"
                           name="fourth">定时任务补偿</el-tab-pane>
              <el-tab-pane label="季节"
                           name="fifth">定时任务补偿</el-tab-pane>
              <el-tab-pane label="活动/节日"
                           name="sixth">
                <el-row>
                  <el-button round
                             size="mini">日常</el-button>
                  <el-button round
                             size="mini">双11</el-button>
                  <el-button round
                             size="mini">年中大促</el-button>
                  <el-button round
                             size="mini">新风尚</el-button>
                  <el-button round
                             size="mini">聚划算</el-button>
                  <el-button round
                             size="mini">品牌团</el-button>
                  <el-button round
                             size="mini">双12</el-button>
                  <el-button round
                             size="mini">天猫运动会</el-button>
                  <el-button round
                             size="mini">女王节</el-button>
                  <el-button round
                             size="mini">中秋节</el-button>
                  <el-button round
                             size="mini">出游季</el-button>
                  <el-button round
                             size="mini">儿童节</el-button>
                  <el-button round
                             size="mini">开学季</el-button>
                  <el-button round
                             size="mini">感恩节</el-button>
                  <el-button round
                             size="mini">父亲节</el-button>
                  <el-button round
                             size="mini">母亲节</el-button>
                  <el-button round
                             size="mini">年货节</el-button>
                  <el-button round
                             size="mini">情人节</el-button>
                  <el-button round
                             size="mini">闺蜜节</el-button>
                  <el-button round
                             size="mini">端午节</el-button>
                  <el-button round
                             size="mini">圣诞节</el-button>
                  <el-button round
                             size="mini">男人节</el-button>
                </el-row>
              </el-tab-pane>
              <el-tab-pane label="区块标签"
                           name="seventh">定时任务补偿</el-tab-pane>
              <el-tab-pane label="风格标签"
                           name="eighth">定时任务补偿</el-tab-pane>
            </el-tabs>
          </div>
          <div class="main-nav-third">
            <div class="main-nav-third-left">
              <el-row>
                <el-button type="warning"
                           size="mini">时间</el-button>
                <span style="font-size:14px;font-weight:700;margin:0 20px 0 50px;">不限</span>
                <el-button type="text">最新上传</el-button>
                <el-button type="text">最新修改</el-button>
                <el-button type="text">下载量</el-button>
              </el-row>
            </div>
            <div class="main-nav-third-right">
              <el-row>
                <el-button type="primary"
                           size="mini">管理</el-button>
                <el-button type="warning"
                           size="mini">关联多货号</el-button>
                <el-button type="warning"
                           size="mini">上传压缩包</el-button>
                <el-button type="warning"
                           size="mini">上传</el-button>
              </el-row>
            </div>
          </div>
        </div>
        <div class="main-imgs">
          <vue-waterfall-easy :imgsArr="imgsArr"
                              @scrollLoadImg="fetchImgsData"
                              :maxCols=5>
          </vue-waterfall-easy>
        </div>
      </el-main>
      <el-footer></el-footer>
    </el-container>
  </div>
</template>

<script>
import vueWaterfallEasy from 'vue-waterfall-easy'
export default {
  data () {
    return {
      activeIndex: '1',
      activeIndex2: '1',
      radio: '1',
      input: '',
      activeName: 'first',
      imgsArr: [],
      fetchImgsArr: [],
      group: 0
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    },
    handleClick (tab, event) {
      console.log(tab, event)
    },
    initImgsArr (n, m) {
      let arr = []
      for (let i = n; i < m; i++) {
        arr.push({
          src: '/static/logo.png',
          link: '',
          info: ''
        })
        this.group++
      }
      return arr
    },
    fetchImgsData () {
      this.imgsArr = this.imgsArr.concat(this.fetchImgsArr)
    }
  },
  components: {
    vueWaterfallEasy
  },
  created () {
    this.imgsArr = this.initImgsArr(0, 9)
    console.log(this.imgsArr)
    this.fetchImgsArr = this.initImgsArr(10, 20)
  }
}
</script>
<style lang='scss' scoped>
.el-header {
  display: flex;
  justify-content: center;
  padding: 0;
  background: #545c64;
  .el-menu {
    display: inline-block;
  }
}
.el-main {
  padding: 20px 100px;
  .main-nav-first div {
    display: flex;
    justify-content: flex-end;
    height: 40px;
    line-height: 40px;
    .main-nav-result {
      margin-right: 50px;
      span {
        color: #ffd04b;
      }
    }
    .main-nav-radio {
      align-items: center;
      .el-radio {
        margin-right: 20px;
      }
    }
    .man-nav-input {
      width: 250px;
    }
  }
  .main-nav-second {
    margin: 10px 0;
    .el-tabs__nav-scroll {
      background: #ccc;
    }
    .el-button + .el-button {
      margin-bottom: 10px;
    }
  }
  .main-nav-third {
    display: flex;
    justify-content: space-between;
    .ain-nav-third-left {
      .el-button--warning {
        color: #000;
      }
    }
  }
  .main-imgs {
    height: 100vh;
    .vue-waterfall-easy-container {
      .vue-waterfall-easy-scroll {
        overflow-y: hidden;
      }
    }
  }
}
</style>
