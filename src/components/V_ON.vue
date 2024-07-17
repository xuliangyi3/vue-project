<template>
        -----------------------------
        <p>{{ msg }}</p>
        <button @click="count++">ADD</button>
        <p>{{ count }}</p>

        <p>{{ msg1 }}</p>
        <button @click="addCount('hello')">ADD1</button>
        <p>{{ count }}</p>
        <!-- $event表示对象 -->
        <p @click="GetName(fruit,$event)" v-for="fruit,index in fruits" :key="index">{{ fruit }}</p>
        ---------------------------<br>
        <p>事件修饰符</p>
        <a @click.prevent="clickHandler" href="https://www.baidu.com" target="_blank">百度</a>
        <div @click="clickDiv.stop">
            <p @click="clickP">测试冒泡</p>
        </div>

</template>

<script>
export default {
    data() {
        return {
            msg: "事件处理(内联事件处理器)",
            count:0,
            msg1:"事件处理(方法事件处理器)",
            fruits:["苹果","西瓜","香蕉"]
        }
    },
    methods:{
        addCount(e){
            // e.target.innerHTML="Add"+ this.count,
            this.count++,
            console.log(e)
        },
        GetName(name,e){
            console.log(name,e)
        },
        clickHandler(e){
            // e.preventDefault();
            console.log('点击事件')
        },
        clickDiv(){
            console.log("Div")
        },
        clickP(){
            console.log("P")
        }
    }
}
</script>
<style>
#appID{
    color: red;
}
.appClass{
    color: blue;
}
</style>
