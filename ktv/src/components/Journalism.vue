<template>
    <div class="content">
        <div class="topfunction">
            <a href="javascript:;" class="return" @click="back"></a>
            <a href="javascript:;" class="login"></a>
        </div>
        <h2>成都夜场</h2>
        <ul>
            <li v-for="val in listData" :key="val.title">
                <router-link :to="'/newsdetails/' + val.id">
                    <div class="title">{{val.title}}</div>
                    <div class="date"><img src="../assets/img/time.png" alt=""><span>{{val.time}}</span></div>
                </router-link>
            </li>
        </ul>
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
    background-color: #f3f3f3;
    margin-top: 84/@vw;
    .topfunction {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: (84 / @vw);
        display: flex;
        align-items: center;
        justify-content: space-between;
        background-color: #fafafa;
        .return {
            display: block;
            width: (40 / @vw);
            height: (40 / @vw);
            text-align: center;
            line-height: (40 / @vw);
            margin-left: (40 / @vw);
            margin-top: (10 / @vw);
            &::after {
                content: "";
                display: inline-block;
                width: (24 / @vw);
                height: (24 / @vw);
                border-left: 1px solid #444;
                border-top: 1px solid #444;
                transform: rotate(-45deg);
            }
        }
        .login {
            display: block;
            width: (45 / @vw);
            height: (45 / @vw);
            margin-right: (100 / @vw);
            background: url("../assets/img/login.png");
            background-size: 100% 100%;
        }
    }
    &>h2 {
        color: #525252;
        font-size: 26/@vw;
        height: 60/@vw;
        line-height: 60/@vw;
        font-weight: 400;
        margin-bottom: 10/@vw;
        background-color: #fff;
    }
    &>ul {
        margin-bottom: 92/@vw;
        li {
            height: 124/@vw;
            background-color: #fff;
            margin: 0 4/@vw 8/@vw;
            a {
                display: block;
                height: 124/@vw;
                text-align: left;
                padding: 0 20/@vw;
                .title {
                    padding: 10/@vw 0;
                    line-height: 48/@vw;
                    font-size: 28/@vw;
                    color: #222;
                    font-family: "Arial";
                }
                .date {
                    display: flex;
                    align-content: center;
                    img {
                        width: 32/@vw;
                        height: 32/@vw;
                        vertical-align: baseline;
                    }
                    span {
                        color: #999999;
                        font-size: 24/@vw;
                        margin-top: 4/@vw;
                        line-height: 1.2;
                        padding-left: 10/@vw;
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
        this.$http.get('/index.php/api/journalism/list').then(res => {
            this.listData = res
        })
    }
}
</script>