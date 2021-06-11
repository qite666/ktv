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
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: (40 / @vw);
    display: flex;
    align-items: center;
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
        width: 10px;
        height: 10px;
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
      margin: 0 10px;
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
          width: 11px;
          height: 11px;
          border: 1px solid #999;
          border-radius: 50%;
        }
        &::after {
          content: "";
          position: absolute;
          bottom: 0;
          right: 2px;
          width: 1px;
          height: 5px;
          background: #999;
          transform: rotate(-45deg);
        }
      }
      span {
        font-size: 11px;
        color: #ccc;
      }
    }
    .share{
        display: block;
        width: (22 / @vw);
        height: (22 / @vw);
        margin-right: (12 / @vw);
        background: url("../assets/img/share.png");
        background-size: 100% 100%;
    }
    .login{
        display: block;
        width: (22 / @vw);
        height: (22 / @vw);
        margin-right: (12 / @vw);
        background: url("../assets/img/login.png");
        background-size: 100% 100%;
    }
    .homeback{
        display: block;
        width: (22 / @vw);
        height: (22 / @vw);
        margin-right: (12 / @vw);
        background: url("../assets/img/homeback.png");
        background-size: 100% 100%;
    }
  }
  .navmore {
    position: absolute;
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
}
</style>