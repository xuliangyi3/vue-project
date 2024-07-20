<template>
<p>{{ msg }}</p>
<button @click="clickHandle">修改数据</button>
</template>
<script>
export default {
    data(){
        return{
            msg:"侦听器"
        }
    },
    methods:{
        clickHandle(){
            this.msg="你好"
        }
    },
    watch:{
        //newValue:改变之后的数据
        //oldValue:改变之前的数据
        //函数名必须跟侦听的数据对象名称一致
        msg(newValue,oldValue){
            //数据发生变化自动执行
            console.log("newValue:"+newValue,"oldValue:"+oldValue)
        }
    }
}
</script>