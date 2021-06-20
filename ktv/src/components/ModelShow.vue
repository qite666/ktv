<template>
  <div class="content">
    <div class="topfunction">
      <a href="javascript:;" class="return" @click="back"></a>
      <div class="seach">
        <i></i>
        <span>请输入您要搜索的内容</span>
      </div>
      <a href="javascript:;" class="share"></a>
      <a href="javascript:;" class="login"></a>
      <a href="javascript:;" class="homeback"></a>
    </div>
    <div class="topmodel">
      <a href="javascript:;">高端模特</a>
    </div>
    <div class="center">
      <ul>
        <li v-for="val in listData" :key="val.id">
          <router-link :to="/modelshow2/ + val.id">{{val.title}}</router-link>
          <span>￥{{val.price}}</span>
        </li>
      </ul>
    </div>
    <div class="navmore" @click="navFlag">
            <i></i>
            <i></i>
            <i></i>
        </div>
        <nav @click="navFlag" v-if="navflag">
            <ul>
                <li>
                    <router-link to="/index">首页</router-link>
                </li>
                <li>
                    <router-link to="/journalism">夜场新闻</router-link>
                </li>
                <li>
                    <router-link to="/aboutus">联系我们</router-link>
                </li>
                <li>
                    <router-link to="/modelshow">模特展示</router-link>
                </li>
            </ul>
        </nav>
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
      width: (120 / @vw);
      height: (44 / @vw);
      margin-right: (30 / @vw);
      background: url("../assets/img/share.png");
      background-size: 100% 100%;
    }
    .login {
      display: block;
      width: (120 / @vw);
      height: (44 / @vw);
      margin-right: (30 / @vw);
      background: url("../assets/img/login.png");
      background-size: 100% 100%;
    }
    .homeback {
      display: block;
      width: (120 / @vw);
      height: (44 / @vw);
      margin-right: (80 / @vw);
      background: url("../assets/img/homeback.png");
      background-size: 100% 100%;
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
      width: (247 / @vw);
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
    ul {
      width: 100%;
      height: 100%;
      li {
        width: (1516 / @vw);
        height: (160 / @vw);
        background-color: #fff;
        text-align: left;
        border-bottom: 1px solid #eee;
        a {
          display: block;
          width: 100%;
          height: (88 / @vw);
          line-height: (88 / @vw);
          font-size: (28 / @vw);
          margin-bottom: (10 / @vw);
          padding-left: (20 / @vw);
        }
        span {
          overflow: hidden;
          display: block;
          height: (30 / @vw);
          line-height: (32 / @vw);
          font-size: (32 / @vw);
          color: #f00;
          font-weight: 600;
          padding-left: (20 / @vw);
        }
      }
    }
  }
  .navmore {
        position: fixed;
        z-index: 1;
        top: (4 / @vw);
        right: 8/@vw;
        width: (64 / @vw);
        height: (64 / @vw);
        border: 1px solid #3cb5d5;
        border-radius: (64 / @vw);
        background-color: #fff;
        i {
            display: block;
            width: (44 / @vw);
            height: (4 / @vw);
            margin: (12 / @vw) auto 0;
            background-color: #3cb5d5;
        }
    }
    nav {
        position: fixed;
        top: 0;
        left: 0;
        width: 750/@vw;
        height: 100%;
        background: rgba(0, 0, 0, .5);
        ul {
            width: 450/@vw;
            float: right;
            height: 100%;
            padding: 20/@vw 0;
            box-shadow: -2px 0 5px #000;
            li {
                margin: 30/@vw;
                border-bottom: 4/@vw solid #45494C;
                a {
                    display: block;
                    font-size: 34/@vw;
                    color: #fff;
                    text-align: left;
                    padding: 10/@vw 0 10/@vw 50/@vw ;
                }
            }
        }
    }
}
</style>
<script>
export default {
    data () {
        return {
            listData: [],
            navflag: false
        }
    },
    methods: {
        gettype (id) {
            this.$http.get('/index.php/api/journalism/list?pageNumber=1&pageSize=21&journalismtypeid=' + id).then(res => {
                console.log(res)
                this.listData = res
            })
        },
        navFlag () {
            if (this.navflag) {
                this.navflag = false
            } else {
                this.navflag = true
            }
        },
        back () {
            this.$router.go(-1)
        }
    },
    mounted () {
      this.$http.get('http://49.235.93.38:82/index.php/api/models/list').then(res => {
        if (res) {
          this.listData = res
        }
      })
    }
}
</script>