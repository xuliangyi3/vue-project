<template>
    <h3>模板引用</h3>
    <h4>对DOM</h4>
    <div ref="container" class="container">{{ msg }}</div>
    <button @click="getElementHandle">获取DOM</button>
</template>
<script>

/*
DOM的操作
    内容改变{{ 模板语法 }}
    属性改变:v-bind:指令
    事件:v-on
如果没有特别需求,不要操作DOM
*/
export default {
    data() {
        return {
            msg: '内容'
        }
    },
    methods: {
        getElementHandle() {
            console.log(this.$refs.container.innerHTML='哈哈哈哈');
        }
    }
}
</script>