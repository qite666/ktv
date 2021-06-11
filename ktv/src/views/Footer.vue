<template>
<div>
  <footer>
    <ul>
      <li>
        <a href="javascript:;" class="current">
          <img src="../assets/img/tu1.png" alt="">
          <span>首页</span>
        </a>
      </li>
      <li>
        <a href="tel:13688143752">
          <img src="../assets/img/tu2.png" alt="">
          <span>电话</span>
        </a>
      </li>
      <li>
        <a href="javascript:;">
          <img src="../assets/img/tu3.png" alt="">
          <span>微信咨询</span>
        </a>
      </li>
    </ul>
    <div class="wxServerAlt">
      <div class="altMain">
        <div><img src="../assets/img/tu4.png" alt=""></div>
        <span>长按识别二维码</span>
      </div>
    </div>
  </footer>
</div>
</template>
<style lang="less">
@import "../assets/css/reset.css";
@screenWidth:750;
@vw:(@screenWidth/100vw);
footer {
  position: fixed;
  left: 50%;
  margin-left: -50%;
  bottom: 0;
  width: 100%;
  height: 92/@vw;
  background-color: rgba(0, 0, 0, 0.6);
  ul {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100%;
    li {
      width: 33%;
      height: 100%;
      a {
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        img {
          width: 40/@vw;
        }
        span {
          font-size: 24/@vw;
          color: #fff;
        }
      }
      .current {
        span {
          color: #3cb5d5;
        }
      }
    }
  }
  .wxServerAlt {
    position: fixed;
    top: 50%;
    left: 50%;
    margin: -775/@vw 0 0 -375/@vw;
    width: 750/@vw;
    height: 1550/@vw;
    background-color: rgba(0, 0, 0, 0.3);
    .altMain {
      position: absolute;
      top: 50%;
      left: 50%;
      margin: -250/@vw 0 0 -220/@vw;
      padding: 40/@vw;
      width: 440/@vw;
      height: 500/@vw;
      background-color: #fff;
      box-sizing: border-box;
      border-radius: 10/@vw;
      div {
        width: 360/@vw;
        height: 360/@vw;
        margin-bottom: 30/@vw;
        img {
          width: 100%;
          height: 100%;
        }
      }
      span {
        font-size: 24/@vw;
        color: #222;
      }
    }
  }
}
</style>
