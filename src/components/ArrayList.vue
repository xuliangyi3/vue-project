<template>
    <p>{{ msg }}</p>
    <button @click="addListHandle">添加数据</button>
    <ul v-for="name,index of names" :key="index">
        <li>{{ name }}</li>
    </ul>
    <button @dblclick.once="concatLiskHandle">合并数组(双击)</button>
    <p>数组1</p>
    <p v-for="num,index of num1" :key="index">{{ num }}</p>
    <p>数组2</p>
    <p v-for="num,index of num2" :key="index">{{ num }}</p>
</template>
<script>
export default{
    data(){
        return{
            msg:"数组变化侦测",
            names:["苹果",'西瓜','香蕉'],
            num1:[1,2,3,4,5],
            num2:[6,7,8,9,10],
        }
    },
    methods:{
        addListHandle(){
            //引起ui自动更新
            this.names.push('火龙果')

            //不会引起ui自动更新
            // this.names.concat(['火龙果'])
        },
        concatLiskHandle(){
           this.num1 = this.num1.concat(this.num2)
        }
    }
}
</script>