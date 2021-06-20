<template>
    <div>
        <keep-alive exclude="newsdetails,aboutus2,model2">
            <router-view></router-view>
        </keep-alive>
        <my-foot></my-foot>
    </div>
</template>
<script>
import myFoot from './Footer'
export default {
    components: {
        myFoot: myFoot
    }
}
</script>