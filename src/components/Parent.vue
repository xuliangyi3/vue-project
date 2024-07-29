<template>
    <h3>Parent</h3>
    <Child :value="msg" :int="int" :array="array" :obj="object"/>
</template>

<script>
import Child from './Child.vue';
export default {
    components: {
        Child,
    },
    data() {
        return {
            msg: "组件传递数据",
            int:20,
            array:['苹果','西瓜','香蕉'],
            object:{
                name:"周杰伦",
                song:"《爱才七元钱》"
            }
        }
    }
}
</script>