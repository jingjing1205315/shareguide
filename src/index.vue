<template>
    <div class='index'>
        <div @click="clickbtn">111111ls{{text}}</div>
    </div>
</template>

<script>
export default {
    name: "shareGuide",
    data: function () {
        return {};
    },
    props: ['text'],
    methods: {
        clickbtn(){
            console.log('clickbtn', this);
            this.$emit('closeShareGuide')
        }
    },
    components: {},
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
    }

}
</style>