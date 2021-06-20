<template>
  <div class="content">
    <div class="scrollfixed">
      <ul>
        <li @click="back">
          <span></span>
        </li>
        <li>
          <p>商品</p>
          <p>详情</p>
        </li>
        <li>
          <img src="../assets/img/ellipsisMenu2.png" alt="" />
        </li>
      </ul>
    </div>
    <div class="fixedleft">
      <div>
        <span></span>
      </div>
    </div>
    <div class="fixedright">
      <img src="../assets/img/ellipsisMenu.png" alt="" />
    </div>
    <div class="centerimg">
      <img :src="imgUrl + img" alt="" />
    </div>
    <div class="center">
      <div class="contertop">
        <div class="head">
          <div class="head-l">
            <span>￥</span>
            <span>1500</span>
          </div>
          <div class="head-r">
            <img src="../assets/img/share2.png" alt="" />
            <p>推荐</p>
          </div>
        </div>
        <div class="bot">
          <p>成都夜总会模特</p>
        </div>
      </div>
      <div class="description">
        <div class="detiontop">
          <h2>产品说明</h2>
        </div>
        <div class="detionimg">
          <img :src="imgUrl + img" alt="" />
        </div>
      </div>
      <div class="related">
        <div class="relatedtop">
          <h2>相关产品</h2>
        </div>
        <div class="relatedoption">
          <ul>
            <li v-for="val in relatedData" :key="val.id" @click="getData(val.id)">
              <img :src="imgUrl + val.image" alt="" />
              <i>{{val.title}}</i>
              <div class="optionprice">
                <span>￥</span>
                <span>{{val.price}}</span>
              </div>
            </li>
          </ul>
        </div>
      </div>
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
  .scrollfixed {
    width: 100%;
    height: (110 / @vw);
    background-color: #fff;
    ul {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: (690 / @vw);
      height: (110 / @vw);
      margin: 0 auto;
      li {
        &:nth-of-type(1) {
          width: (45 / @vw);
          height: (45 / @vw);
          display: flex;
          align-items: center;
          span {
            display: block;
            width: (22 / @vw);
            height: (22 / @vw);
            border-left: 2px solid #000;
            border-top: 2px solid #000;
            transform: rotate(-45deg);
          }
        }
        &:nth-of-type(2) {
          display: flex;
          align-items: center;
          justify-content: space-evenly;
          width: (610 / @vw);
          height: (68 / @vw);
          p {
            display: block;
            font-size: (30 / @vw);
            font-weight: 400;
            padding-bottom: (10 / @vw);
            color: #606060;
            &:hover {
              color: #000;
              font-weight: 700;
              border-bottom: (3 / @vw) solid #0082ff;
            }
          }
        }
        &:nth-of-type(3) {
          width: (33 / @vw);
          height: (37 / @vw);
          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
  .fixedleft {
    position: fixed;
    top: (25 / @vw);
    left: (17 / @vw);
    width: (60 / @vw);
    height: (60 / @vw);
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: (60 / @vw);
    display: none;
    div {
      width: (20 / @vw);
      height: (20 / @vw);
      margin: 50% auto 0;
      transform: translateY(-50%);
      span {
        display: block;
        width: 100%;
        height: 100%;
        border-left: 2px solid #fff;
        border-top: 2px solid #fff;
        transform: rotate(-45deg);
      }
    }
  }
  .fixedright {
    position: fixed;
    top: (25 / @vw);
    right: (17 / @vw);
    width: (60 / @vw);
    height: (60 / @vw);
    border-radius: (60 / @vw);
    background-color: rgba(0, 0, 0, 0.5);
    display: none;
    img {
      width: (32 / @vw);
      height: (7 / @vw);
      margin: 50% auto 0;
      transform: translateY(-50%);
    }
  }
  .centerimg {
    width: 100%;
    height: (750 / @vw);
    overflow: hidden;
    position: relative;
    img {
      width: 100%;
      height: auto !important;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
  .center {
    width: 100%;
    margin-bottom: 92/@vw;
    background-color: #eee;
    .contertop {
      width: 100%;
      height: (214 / @vw);
      padding-top: (32 / @vw);
      background-color: #fff;
      margin-bottom: (20 / @vw);
      .head {
        display: flex;
        justify-content: space-between;
        width: (696 / @vw);
        height: (80 / @vw);
        margin: 0 auto (20 / @vw);
        .head-l {
          display: flex;
          align-items: center;
          justify-content: space-between;
          width: (162 / @vw);
          height: (66 / @vw);
          span:nth-of-type(1) {
            display: block;
            font-size: (30 / @vw);
            color: #fa230a;
          }
          span:nth-of-type(2) {
            display: block;
            font-size: (50 / @vw);
            color: #fa230a;
          }
        }
        .head-r {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-wrap: wrap;
          width: (48 / @vw);
          height: (40 / @vw);
          img {
            width: (36 / @vw);
            height: (36 / @vw);
            margin-bottom: (10 / @vw);
          }
          p {
            color: #888;
            font-size: (22 / @vw);
          }
        }
      }
      .bot {
        width: (696 / @vw);
        height: (80 / @vw);
        margin: (30 / @vw) auto 0;
        text-align: left;
        p {
          font-size: (32 / @vw);
          color: #2a2a2a;
          font-weight: 700;
        }
      }
    }
    .description {
      width: 100%;
      height: (1006 / @vw);
      background-color: #fff;
      margin-bottom: (30 / @vw);
      .detiontop {
        width: 100%;
        height: (52 / @vw);
        padding: (30 / @vw) 0 (20 / @vw);
        display: flex;
        justify-content: center;
        h2 {
          font-size: (28 / @vw);
          color: #2a2a2a;
          border-bottom: (6 / @vw) solid #0082ff;
        }
      }
      .detionimg {
        width: (700 / @vw);
        height: (874 / @vw);
        margin: 0 auto;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
    .related {
      width: 100%;
      padding: (34 / @vw) 0 (30 / @vw);
      background-color: #fff;
      .relatedtop {
        width: (700 / @vw);
        height: (34 / @vw);
        margin: 0 auto (20 / @vw);
        text-align: left;
        h2 {
          font-size: (26 / @vw);
          color: #2a2a2a;
          font-weight: 700;
        }
      }
      .relatedoption {
        width: (700 / @vw);
        margin: 0 auto;
        ul {
          display: flex;
          flex-wrap: wrap;
          justify-content: space-between;
          width: 100%;
          li {
            width: (220 / @vw);
            height: (342 / @vw);
            img {
              width: 100%;
              height: (220 / @vw);
              margin-bottom: (18 / @vw);
            }
            i {
              display: block;
              width: 100%;
              height: (70 / @vw);
              font-size: (24 / @vw);
            }
            .optionprice {
              display: flex;
              width: 100%;
              height: (34 / @vw);
              span:nth-of-type(1) {
                display: block;
                color: #fa230a;
                padding-right: (10 / @vw);
              }
              span:nth-of-type(2) {
                display: block;
                font-size: (26 / @vw);
                color: #fa230a;
                font-weight: 600;
              }
            }
          }
        }
      }
    }
  }
}
</style>
<script>
export default {
    name: 'model2',
    data () {
        return {
            data: [],
            relatedData: [],
            index: 0,
            img: '',
            title: '',
            navflag: false
        }
    },
    methods: {
        getData (id) {
            this.relatedData = this.data.filter(val => id !== val.id)
            this.index = this.data.findIndex(val => id === val.id)
            this.img = this.data[this.index].image
            this.title = this.data[this.index].title
        },
        back () {
            this.$router.go(-1)
        }
    },
    mounted () {
        var id = parseInt(this.$route.params.id)
        this.$http.get('http://49.235.93.38:82/index.php/api/models/list').then(res => {
            if (res) {
                this.data = res
                this.relatedData = this.data.filter(val => id !== val.id)
                this.index = this.data.findIndex(val => id === val.id)
                this.img = this.data[this.index].image
                this.title = this.data[this.index].title
            }
        })
    }
}
</script>