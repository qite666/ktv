<template>
    <div class="content">
        <div class="topfunction">
            <a href="javascript:;" class="return" @click="back"></a>
            <a href="javascript:;" class="login"></a>
        </div>
        <h2>{{title}}</h2>
        <div><VueMarkdown :source="value"></VueMarkdown></div>
    </div>
</template>
<style lang="less" scoped>
@import '../assets/css/reset.css';
@screenWidth:750;
@vw:(@screenWidth/100vw);
.content {
    width: 750/@vw;
    background-color: #ffffff;
    padding: 10/@vw 10/@vw 122/@vw;
    box-sizing: border-box;
    &>h2 {
        width: 720/@vw;
        color: #333;
        font-weight: bold;
        font-size: 40/@vw;
        line-height: 1.5em;
    }
    &>div {
        width: 720/@vw;
        box-sizing: border-box;
        padding: 10/@vw 38/@vw;
        font-size: 32/@vw;
    }
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
}
</style>
<script>
import VueMarkdown from 'vue-markdown'
export default {
    name: 'aboutus2',
    data () {
        return {
            data: [],
            value: '',
            title: ''
        }
    },
    components: {
        VueMarkdown
    },
    methods: {
        back () {
            this.$router.go(-1)
        }
    },
    mounted () {
        var id = parseInt(this.$route.params.id)
        console.log(id)
        this.$http.get('index.php/api/about_us/list').then(res => {
            if (res) {
                console.log(res)
                this.data = res
                this.index = this.data.findIndex(val => val.id === id)
                this.value = this.data[this.index].content
                this.title = this.data[this.index].title
            }
        })
    }
}
</script>