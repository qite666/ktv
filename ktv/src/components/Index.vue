<template>
    <div class="content">
        <div class="head">
            <img src="../assets/img/title.png" alt="">
        </div>
        <div class="banner">
            <img src="../assets/img/banner.jpg" alt="">
            <!-- <img :src="imgUrl + bannerImg" alt="">
            <div class="discounts">
                <VueMarkdown :source="value"></VueMarkdown>
            </div>
            <div class="qr-code"><img src="" alt=""></div>
            <div class="tel">T：13688143752</div> -->
        </div>
        <div class="circumstances-box">
            <div class="circumstances">
                <h2>ENVIRONMENTAL DISPLAY</h2>
                <p>环境/AMBIENT</p>
                <div class="border"></div>
                <ul class="clearfix">
                    <li v-for="val in environmental" :key="val.image">
                        <a href="javascript:;">
                            <div class="list-top"><img :src="imgUrl + val.image" alt=""></div>
                            <div class="list-btm">
                                <h3>{{val.title}}</h3>
                                <p>联系人：{{val.contacts}}</p>
                                <p>手 机：{{val.phone}}</p>
                                <p>地 址：成都</p>
                            </div>
                            <div class="more"><a href="tel:13688143752">查看更多</a></div>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="about-box">
            <div class="about">
                <h2>KTV夜总会招聘</h2>
                <p>小包低消1080元 中包低消1280 大包低消1380 豪包低消2680全场所有啤酒均可享受买二送一，还有更多豪礼等着你，当晚本包间消费满6666以上，当晚可赠送豪华名宿酒店一套，限当天使用。</p>
            </div>
        </div>
        <div class="model-box">
            <div class="model">
                <h2>高端KTV</h2>
                <p>High-end KTV</p>
                <div class="border"></div>
                <ul>
                    <li v-for="val in modelData" :key="val.id">
                        <router-link :to="'/modelshow2/' + val.id">
                            <img :src="imgUrl + val.image" alt="">
                            <p>{{val.title}}</p>
                        </router-link>
                    </li>
                </ul>
            </div>
        </div>
        <div class="journalism-box">
            <div class="journalism">
                <h2>高端KTV新闻</h2>
                <p>High-end KTV News</p>
                <div class="border"></div>
                <ul>
                    <li v-for="val in journalism" :key="val.id">
                        <router-link :to="'/newsdetails/' + val.id">
                            <h2>{{val.title}}</h2>
                        </router-link>
                    </li>
                </ul>
            </div>
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
@import '../assets/css/reset.css';
@screenWidth:750;
@vw:(@screenWidth/100vw);
.content {
    width: 750/@vw;
    .head {
        width: 100%;
        img {
            display: block;
            width: 100%;
        }
    }
    .banner {
        width: 100%;
        img {
            display: block;
            width: 100%;
        }
    }
    .about-box {
        width: 750/@vw;
        height: 888/@vw;
        background: url('../assets/img/image_12.jpeg') no-repeat center;
        background-size: 100% 100%;
        .about {
            width: 750/@vw;
            height: 888/@vw;
            background-color: rgba(0, 0, 0, .5);
            &>h2 {
                padding-top: 200/@vw;
                color: #fff;
                font-size: 44/@vw;
                font-family: SimSun;
            }
            &>p {
                width: 560/@vw;
                margin: 48/@vw auto;
                font-weight: bold;
                font-family: SimSun;
                font-size: 32/@vw;
                color: #fff;
                line-height: 1.5;
                margin-bottom: 16/@vw;
            }
        }
    }
    .circumstances-box {
        width: 100%;
        background-color: #f3f3f3;
        .circumstances {
            width: 100%;
            border: 1px solid transparent;
            box-sizing: border-box;
            h2 {
                padding-top: 48/@vw;
                color: #333333;
                font-size: 44/@vw;
                font-family: SimSun;
            }
            p {
                font-weight: bold;
                font-family: SimSun;
                font-size: 32/@vw;
                color: #989898;
                line-height: 1.75;
                margin-bottom: 16/@vw;
            }
            .border {
                width: 72/@vw;
                height: 2px;
                margin: 0 auto 32/@vw;
                background-color: rgb(60, 181, 213);
            }
            ul {
                li {
                    width: 706/@vw;
                    margin: 0 20/@vw 30/@vw;
                    a {
                        position: relative;
                        display: block;
                        width: 100%;
                        height: 740/@vw;
                        background-color: #fff;
                        .list-top {
                            width: 100%;
                            img {
                                display: block;
                                width: 100%;
                            }
                        }
                        .list-btm {
                            width: 100%;
                            height: 266/@vw;
                            padding: 20/@vw 0;
                            box-sizing: border-box;
                            overflow: hidden;
                            h3 {
                                margin-bottom: 8/@vw;
                                font-weight: bold;
                                font-family: SimSun;
                                font-size: 32/@vw;
                                color: #333333;
                                line-height: 56/@vw;
                            }
                            p {
                                font-size: 28/@vw;
                                color: #989898;
                                line-height: 48/@vw;
                                margin: 0;
                            }
                            .list-btm-btm {
                                display: flex;
                                justify-content: space-between;
                                align-items: center;
                                padding: 26px 36px 0;
                                color: #989898;
                                font-size: 14px;
                                line-height: 1.8;
                                img {
                                    width: auto;
                                }
                            }
                        }
                        .more {
                            position: absolute;
                            bottom: 0;
                            left: 50%;
                            margin-left: -375/@vw;
                            width: 750/@vw;
                            height: 60/@vw;
                            line-height: 60/@vw;
                            border-radius: 8/@vw;
                            overflow: hidden;
                            a {
                                background-color: #c00;
                                font-family: "微软雅黑";
                                font-size: 28/@vw;
                                color: #fff;
                            }
                        }
                    }
                }
            }
        }
    }
    .model-box {
        width: 100%;
        .model {
            width: 100%;
            border: 1px solid transparent;
            box-sizing: border-box;
            &>h2 {
                padding-top: 48/@vw;
                color: #333333;
                font-size: 44/@vw;
                font-family: SimSun;
            }
            &>p {
                font-weight: bold;
                font-family: SimSun;
                font-size: 32/@vw;
                color: #989898;
                line-height: 1.75;
                margin-bottom: 16/@vw;
            }
            .border {
                width: 72/@vw;
                height: 2px;
                margin: 0 auto 32/@vw;
                background-color: rgb(60, 181, 213);
            }
            ul {
                display: flex;
                flex-wrap: wrap;
                justify-content: space-evenly;
                li {
                    width: 344/@vw;
                    a {
                        display: block;
                        img {
                            height: 600/@vw;
                            display: block;
                            width: 100%;
                        }
                        p {
                            height: 72/@vw;
                            line-height: 72/@vw;
                            font-family: Arial;
                            font-size: 32/@vw;
                            color: #555555;
                            margin-bottom: 10/@vw;
                        }
                    }
                }
            }
        }
    }
    .journalism-box {
        width: 100%;
        .journalism {
            width: 100%;
            &>h2 {
                padding-top: 48/@vw;
                color: #333333;
                font-size: 44/@vw;
                font-family: SimSun;
            }
            &>p {
                font-weight: bold;
                font-family: SimSun;
                font-size: 32/@vw;
                color: #989898;
                line-height: 1.75;
                margin-bottom: 16/@vw;
            }
            .border {
                width: 72/@vw;
                height: 2px;
                margin: 0 auto 32/@vw;
                background-color: rgb(60, 181, 213);
            }
            ul {
                padding-bottom: 92/@vw;
                border: 1px solid #ccc;
                li {
                    width: 100%;
                    list-style: disc;
                    height: 42/@vw;
                    line-height: 42/@vw;
                    border-bottom: 1px solid #ccc;
                    a {
                        display: block;
                        text-align: left;
                        margin-left: 40/@vw;
                        font-size: 32/@vw;
                        h2 {
                            color: #7C7B7C;
                        }
                    }
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
// import VueMarkdown from 'vue-markdown'
export default {
    data () {
        return {
            // value: '',
            modelData: [],
            journalism: [],
            bannerImg: '',
            environmental: [],
            navflag: false
        }
    },
//   components: {
//     VueMarkdown
//   },
    methods: {
        navFlag () {
            if (this.navflag) {
                this.navflag = false
            } else {
                this.navflag = true
            }
        }
    },
    mounted () {
        // 轮播图
        this.$http.get('index.php/api/carousel_map/list').then(res => {
            this.value = res[0].content
            this.bannerImg = res[0].image
        })
        this.$http.get('index.php/api/ambient/list').then(res => {
            if (res) {
                this.environmental = res.filter((val, index) => val.id <= 3)
            }
        })
        this.$http.get('index.php/api/models/list').then(res => {
            this.modelData = res.filter((val, index) => index <= 5)
        })
        this.$http.get('/index.php/api/journalism/list').then(res => {
            if (res) {
                this.journalism = res
                this.journalism.forEach(val => {
                    val.time = val.time.slice(0, 10)
                })
            }
        })
    }
}
</script>