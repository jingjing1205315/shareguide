<template>
    <div class='index'>
        <div @click="clickbtn">333333{{text}}</div>
        <!-- <div>112221111ls{{text}}</div> -->
    </div>
</template>

<script>
import axios from 'axios';
console.log('axios', axios)
export default {
    name: "shareGuide",
    data: function () {
        return {};
    },
    props: ['text'],
    methods: {
        clickbtn(){
            console.log('clickbtn', this.$emit);
            this.$emit('closeShareGuide')
        }
    },
    components: {},
    created(){
        axios.get('https://m2.qschou.com/gateway/v3.0.0/project/index/auth3/d7138678-c40b-401c-b635-abdfa484d527?share_no=&debug_track_id=17762280ca5a6d-02c6cc32bda82-2164346a-51ab0-17762280ca6d26&r=0.48752362251926895').then(res => {
            console.log(res)
        })
    }
};
</script>

<style lang="less" scoped>
.index{
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    div{
        background: rgba(0,0,0, 0.6);
        width: fit-content;
        margin: 0 auto;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        color:#fff;
    }

}
</style>