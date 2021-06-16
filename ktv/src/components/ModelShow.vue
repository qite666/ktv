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
    height: (40 / @vw);
    display: flex;
    align-items: center;
    background-color: #fff;
    .return {
      display: block;
      width: (15 / @vw);
      height: (20 / @vw);
      text-align: center;
      line-height: (20 / @vw);
      margin-left: (10 / @vw);
      &::after {
        content: "";
        display: inline-block;
        width: (10 / @vw);
        height: (10 / @vw);
        border-left: 1px solid #444;
        border-top: 1px solid #444;
        transform: rotate(-45deg);
      }
    }
    .seach {
      display: flex;
      justify-content: center;
      align-items: center;
      width: (570 / @vw);
      height: (30 / @vw);
      margin: 0 (10 / @vw);
      background-color: #f2f2f2;
      border-radius: (30 / @vw);
      i {
        position: relative;
        display: block;
        width: (15 / @vw);
        height: (15 / @vw);
        &::before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          width: (11 / @vw);
          height: (11 / @vw);
          border: 1px solid #999;
          border-radius: 50%;
        }
        &::after {
          content: "";
          position: absolute;
          bottom: 0;
          right: (2 / @vw);
          width: 1px;
          height: (5 / @vw);
          background: #999;
          transform: rotate(-45deg);
        }
      }
      span {
        font-size: (11 / @vw);
        color: #ccc;
      }
    }
    .share {
      display: block;
      width: (22 / @vw);
      height: (22 / @vw);
      margin-right: (12 / @vw);
      background: url("../assets/img/share.png");
      background-size: 100% 100%;
    }
    .login {
      display: block;
      width: (22 / @vw);
      height: (22 / @vw);
      margin-right: (12 / @vw);
      background: url("../assets/img/login.png");
      background-size: 100% 100%;
    }
    .homeback {
      display: block;
      width: (22 / @vw);
      height: (22 / @vw);
      margin-right: (12 / @vw);
      background: url("../assets/img/homeback.png");
      background-size: 100% 100%;
    }
  }
  .navmore {
    position: fixed;
    top: (2 / @vw);
    right: 0;
    width: (32 / @vw);
    height: (32 / @vw);
    border: 1px solid #3cb5d5;
    border-radius: (32 / @vw);
    i {
      display: block;
      width: (22 / @vw);
      height: (2 / @vw);
      margin: (6 / @vw) auto 0;
      background-color: #3cb5d5;
    }
  }
  .topmodel {
    width: 100%;
    height: (30 / @vw);
    margin-top: (40 / @vw);
    background-color: #fff;
    text-align: left;
    border-bottom: (5 / @vw) solid #eee;
    a {
      display: block;
      width: (247 / @vw);
      height: (30 / @vw);
      text-align: center;
      line-height: (30 / @vw);
      font-size: (13 / @vw);
      color: #525252;
    }
  }
  .center {
    width: 100%;
    height: (558 / @vw);
    overflow: hidden;
    li {
      width: (758 / @vw);
      height: (93 / @vw);
      background-color: #fff;
      text-align: left;
      margin-left: (10 / @vw);
      border-bottom: 1px solid #eee;
      a {
        display: block;
        width: 100%;
        height: (44 / @vw);
        font-size: (14 / @vw);
        margin-bottom: (5 / @vw);
        padding-left: (10 / @vw);
      }
      span {
        display: block;
        font-size: (15 / @vw);
        color: #f00;
        font-weight: 600;
        padding-left: (10 / @vw);
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