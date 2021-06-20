<template>
    <div class="box">
        <div class="topfunction">
            <a href="javascript:;" class="return" @click="back"></a>
            <a href="javascript:;" class="login"></a>
        </div>
        <div class="content">
            <h2>{{title}}</h2>
            <div><VueMarkdown :source="value"></VueMarkdown></div>
        </div>
        <div class="recommend">
            <h2>———————————— <span> 推荐 </span> ————————————</h2>
            <ul>
                <li>
                    <a href="https://sns.qzone.qq.com/cgi-bin/qzshare/cgi_qzshare_onekey?url=http%3A%2F%2Fm.comektv.com%2Fyczp1%2Fwap_doc%2F20099519.html%3Fmember_id%3D%26user_id%3D1913406%26code%3Dd41d8cd98f00b204e9800998ecf8427e" target="_blank">
                        <img src="../assets/img/kj_icon.jpg" alt="">
                        <p>QQ空间</p>
                    </a>
                </li>
                <li>
                    <a href="https://service.weibo.com/share/share.php?title=%E5%A4%9C%E5%9C%BA%E6%8B%9B%E8%81%98%E7%94%B7%E5%A3%AB%E9%9D%A2%E8%AF%95%E8%A6%81%E6%B1%82%E6%80%8E%E4%B9%88%E5%92%8C%E9%A2%86%E7%8F%AD%E7%9B%B8%E5%A4%84_%E6%88%90%E9%83%BD%E9%94%A6%E7%BC%98%E5%9B%BD%E9%99%85%E5%A4%9C%E6%80%BB%E4%BC%9A&url=http%3A%2F%2Fm.comektv.com%2Fyczp1%2Fwap_doc%2F20099519.html%3Fmember_id%3D%26user_id%3D1913406%26code%3Dd41d8cd98f00b204e9800998ecf8427e&source=bookmark#_loginLayer_1623850404638" target="_blank">
                        <img src="../assets/img/weibo.png" alt="">
                        <p>新浪微博</p>
                    </a>
                </li>
                <li>
                    <a href="http://widget.renren.com/dialog/share?resourceUrl=http%3A%2F%2Fm.comektv.com%2Fyczp1%2Fwap_doc%2F20099519.html%3Fmember_id%3D%26user_id%3D1913406%26code%3Dd41d8cd98f00b204e9800998ecf8427e&srcUrl=http%3A%2F%2Fm.comektv.com%2Fyczp1%2Fwap_doc%2F20099519.html%3Fmember_id%3D%26user_id%3D1913406%26code%3Dd41d8cd98f00b204e9800998ecf8427e&title=%E5%A4%9C%E5%9C%BA%E6%8B%9B%E8%81%98%E7%94%B7%E5%A3%AB%E9%9D%A2%E8%AF%95%E8%A6%81%E6%B1%82%E6%80%8E%E4%B9%88%E5%92%8C%E9%A2%86%E7%8F%AD%E7%9B%B8%E5%A4%84_%E6%88%90%E9%83%BD%E9%94%A6%E7%BC%98%E5%9B%BD%E9%99%85%E5%A4%9C%E6%80%BB%E4%BC%9A&description=%E5%A4%9C%E5%9C%BA%E6%8B%9B%E8%81%98%E7%94%B7%E5%A3%AB%E9%9D%A2%E8%AF%95%E8%A6%81%E6%B1%82%E6%80%8E%E4%B9%88%E5%92%8C%E9%A2%86%E7%8F%AD%E7%9B%B8%E5%A4%84_%E6%88%90%E9%83%BD%E9%94%A6%E7%BC%98%E5%9B%BD%E9%99%85%E5%A4%9C%E6%80%BB%E4%BC%9A" target="_blank">
                        <img src="../assets/img/renren.png" alt="">
                        <p>人人网</p>
                    </a>
                </li>
                <li>
                    <a href="https://accounts.douban.com/passport/login?redir=https%3A//www.douban.com/share/service%3Fhref%3Dhttp%253A%252F%252Fm.comektv.com%252Fyczp1%252Fwap_doc%252F20099519.html%253Fmember_id%253D%2526user_id%253D1913406%2526code%253Dd41d8cd98f00b204e9800998ecf8427e%26name%3D%25E5%25A4%259C%25E5%259C%25BA%25E6%258B%259B%25E8%2581%2598%25E7%2594%25B7%25E5%25A3%25AB%25E9%259D%25A2%25E8%25AF%2595%25E8%25A6%2581%25E6%25B1%2582%25E6%2580%258E%25E4%25B9%2588%25E5%2592%258C%25E9%25A2%2586%25E7%258F%25AD%25E7%259B%25B8%25E5%25A4%2584_%25E6%2588%2590%25E9%2583%25BD%25E9%2594%25A6%25E7%25BC%2598%25E5%259B%25BD%25E9%2599%2585%25E5%25A4%259C%25E6%2580%25BB%25E4%25BC%259A%26text%3D%25E5%25A4%259C%25E5%259C%25BA%25E6%258B%259B%25E8%2581%2598%25E7%2594%25B7%25E5%25A3%25AB%25E9%259D%25A2%25E8%25AF%2595%25E8%25A6%2581%25E6%25B1%2582%25E6%2580%258E%25E4%25B9%2588%25E5%2592%258C%25E9%25A2%2586%25E7%258F%25AD%25E7%259B%25B8%25E5%25A4%2584_%25E6%2588%2590%25E9%2583%25BD%25E9%2594%25A6%25E7%25BC%2598%25E5%259B%25BD%25E9%2599%2585%25E5%25A4%259C%25E6%2580%25BB%25E4%25BC%259A" target="_blank">
                        <img src="../assets/img/dou.png" alt="">
                        <p>豆瓣</p>
                    </a>
                </li>
            </ul>
            <div class="flip-over">
                <a href="javascript:;" @click="getData('减')">上一篇</a>
                <a href="javascript:;" @click="getData('加')">下一篇</a>
            </div>
        </div>
    </div>
</template>
<style lang="less" scoped>
@import '../assets/css/reset.css';
@screenWidth:750;
@vw:(@screenWidth/100vw);
.box {
    margin-bottom: 92/@vw;
    background-color: #f7f7f7;
    .content {
        width: 750/@vw;
        padding: 20/@vw;
        margin-bottom: 20/@vw;
        margin-top: 84/@vw;
        box-sizing: border-box;
        background-color: #fff;
        overflow: hidden;
        &>h2 {
            padding: 20/@vw 0;
            line-height: 60/@vw;
            font-size: 40/@vw;
            font-weight: bold;
            color: #222;
        }
        &>div {
            text-align: left;
            font-size: 24/@vw;
            line-height: 50/@vw;
            color: rgb(34, 34, 34);
            font-family: Arial, Verdana, sans-serif;
            font-size: 12px;
        }
    }
    .recommend {
        background-color: #fff;
        &>h2 {
            height: 80/@vw;
            line-height: 72/@vw;
            margin-bottom: 20/@vw;
            position: relative;
            color: #DBDBDB;
            span {
                font-size: 32/@vw;
                padding: 4/@vw 20/@vw;
                color: #222;
            }
        }
        &>ul {
            width: 600/@vw;
            margin: 20/@vw auto ;
            overflow: hidden;
            display: flex;
            justify-content: space-evenly;
            align-content: center;
            li {
                a {
                    display: block;
                    img {
                        display: block;
                        width: 88/@vw;
                        height: 88/@vw;
                        margin-bottom: 10/@vw;
                    }
                    p {
                        font-size: 24/@vw;
                        height: 40/@vw;
                        color: #222;
                    }
                }
            }
        }
        .flip-over {
            width: 750/@vw;
            padding: 20/@vw;
            box-sizing: border-box;
            display: flex;
            justify-content: space-between;
            a {
                font-size: 32/@vw;
                height: 80/@vw;
                line-height: 80/@vw;
                text-align: center;
                width: 240/@vw;
                border-radius: 10/@vw;
                border: 1px solid #ccc;
                color: #000;
            }
        }
    }
    .topfunction {
        position: fixed;
        top: 0;
        left: 0;
        width: 750/@vw;
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
}
</style>
<script>
import VueMarkdown from 'vue-markdown'
export default {
    name: 'newsdetails',
    data () {
        return {
            data: [],
            value: '',
            title: '',
            index: 0,
            name: ''
        }
    },
    components: {
        VueMarkdown
    },
    methods: {
        getData (text) {
            if (text === '减') {
                if (this.index > 0) {
                    this.index--
                }
            } else {
                if (this.index < this.data.length - 1) {
                    this.index++
                }
            }
            this.index = parseInt(this.index)
            this.value = this.data[this.index].content
            this.title = this.data[this.index].title
            this.name = this.data[this.index].name
        },
        back () {
            this.$router.go(-1)
        }
    },
    mounted () {
        var id = parseInt(this.$route.params.id)
        this.$http.get('/index.php/api/journalism/list').then(res => {
            if (res) {
                this.data = res
                this.index = this.data.findIndex(val => val.id === id)
                this.value = this.data[this.index].content
                this.title = this.data[this.index].title
                this.name = this.data[this.index].name
            }
        })
    }
}
</script>