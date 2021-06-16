<template>
  <div class="content">
    <div class="topfunction">
      <a href="javascript:;" class="return"></a>
      <div class="seach">
        <i></i>
        <span>请输入您要搜索的内容</span>
      </div>
      <a href="javascript:;" class="share"></a>
      <a href="javascript:;" class="login"></a>
      <a href="javascript:;" class="homeback"></a>
    </div>
    <div class="navmore">
      <i></i>
      <i></i>
      <i></i>
    </div>
    <div class="topmodel">
      <a href="javascript:;">高端模特</a>
    </div>
    <div class="center">
      <ul>
        <li>
          <a href="javascript:;">成都夜总会模特</a>
          <span>￥1500元</span>
        </li>
        <li>
          <a href="javascript:;">成都夜总会模特</a>
          <span>￥1500元</span>
        </li>
        <li>
          <a href="javascript:;">成都夜总会模特</a>
          <span>￥1500元</span>
        </li>
        <li>
          <a href="javascript:;">成都夜总会模特</a>
          <span>￥1500元</span>
        </li>
        <li>
          <a href="javascript:;">成都夜总会模特</a>
          <span>￥1500元</span>
        </li>
        <li>
          <a href="javascript:;">成都夜总会模特</a>
          <span>￥1500元</span>
        </li>
      </ul>
    </div>
  </div>
</template>
<style lang="less" scoped>
@import "../assets/css/reset.css";
@screenWidth: 750;
@vw: (@screenWidth / 100vw);
.setwh(@w: 750, @h: 1448) {
  width: (@w / @vw);
  height: (@h / @vw);
}
.lt(@l: 0, @t: 0) {
  position: absolute;
  left: (@l / @vw);
  top: (@t / @vw);
}
.rt(@r: 0, @t: 0) {
  position: absolute;
  right: (@r / @vw);
  top: (@t / @vw);
}
.lb(@l: 0, @b: 0) {
  position: absolute;
  left: (@l / @vw);
  bottom: (@b / @vw);
}
.rb(@r: 0, @b: 0) {
  position: absolute;
  right: (@r / @vw);
  bottom: (@b / @vw);
}
.cl(@w) {
  position: absolute;
  left: 50%;
  margin-left: (-@w / 2 / @vw);
}

.ct(@h) {
  position: absolute;
  top: 50%;
  margin-top: (-@h / 2 / @vw);
}
body,
html {
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}
.content {
  position: relative;
  min-width: 320px;
  max-width: 750px;
  min-height: 300px;
  overflow: hidden;
  .topfunction {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: (80 / @vw);
    display: flex;
    align-items: center;
    background-color: #fff;
    .return {
      display: block;
      width: (30 / @vw);
      height: (40 / @vw);
      text-align: center;
      line-height: (40 / @vw);
      margin-left: (20 / @vw);
      &::after {
        content: "";
        display: inline-block;
        width: (20 / @vw);
        height: (20 / @vw);
        border-left: 1px solid #444;
        border-top: 1px solid #444;
        transform: rotate(-45deg);
      }
    }
    .seach {
      display: flex;
      justify-content: center;
      align-items: center;
      width: (1140 / @vw);
      height: (60 / @vw);
      margin: 0 (20 / @vw);
      background-color: #f2f2f2;
      border-radius: (60 / @vw);
      i {
        position: relative;
        display: block;
        width: (30 / @vw);
        height: (30 / @vw);
        &::before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          width: (22 / @vw);
          height: (22 / @vw);
          border: 1px solid #999;
          border-radius: 50%;
        }
        &::after {
          content: "";
          position: absolute;
          bottom: 0;
          right: (4 / @vw);
          width: 1px;
          height: (10 / @vw);
          background: #999;
          transform: rotate(-45deg);
        }
      }
      span {
        font-size: (22 / @vw);
        color: #ccc;
      }
    }
    .share {
      display: block;
      width: (44 / @vw);
      height: (44 / @vw);
      margin-right: (24 / @vw);
      background: url("../assets/img/share.png");
      background-size: 100% 100%;
    }
    .login {
      display: block;
      width: (44 / @vw);
      height: (44 / @vw);
      margin-right: (24 / @vw);
      background: url("../assets/img/login.png");
      background-size: 100% 100%;
    }
    .homeback {
      display: block;
      width: (44 / @vw);
      height: (44 / @vw);
      margin-right: (24 / @vw);
      background: url("../assets/img/homeback.png");
      background-size: 100% 100%;
    }
  }
  .navmore {
    display: none;
    position: fixed;
    top: (4 / @vw);
    right: 0;
    width: (64 / @vw);
    height: (64 / @vw);
    border: 1px solid #3cb5d5;
    border-radius: (64 / @vw);
    i {
      display: block;
      width: (44 / @vw);
      height: (4 / @vw);
      margin: (12 / @vw) auto 0;
      background-color: #3cb5d5;
    }
  }
  .topmodel {
    width: 100%;
    height: (60 / @vw);
    margin-top: (80 / @vw);
    background-color: #fff;
    text-align: left;
    border-bottom: (10 / @vw) solid #eee;
    a {
      display: block;
      width: (494 / @vw);
      height: (60 / @vw);
      text-align: center;
      line-height: (60 / @vw);
      font-size: (26 / @vw);
      color: #525252;
    }
  }
  .center {
    width: 100%;
    height: (1116 / @vw);
    overflow: hidden;
    li {
      width: (1516 / @vw);
      height: (194 / @vw);
      background-color: #fff;
      text-align: left;
      margin-left: (20 / @vw);
      border-bottom: 1px solid #eee;
      a {
        display: block;
        width: 100%;
        height: (88 / @vw);
        font-size: (24 / @vw);
        margin-bottom: (10 / @vw);
        padding-left: (20 / @vw);
      }
      span {
        display: block;
        font-size: (30 / @vw);
        color: #f00;
        font-weight: 600;
        padding-left: (20 / @vw);
      }
    }
  }
}
</style>
<script>
export default {
  data () {
    return {
      modelData: []
    }
  },
  mounted () {
    this.$http.get('index.php/api/models/list').then((res) => {
      this.modelData = res.filter((val, index) => index <= 5)
    })
  }
}
</script>