<template>
    <h3>Parent</h3>
    <Child :value="msg"/>
</template>

<script>
import Child from './Child.vue';
export default {
    components: {
        Child,
    },
    data() {
        return {
            msg: "组件传递数据"
        }
    }
}
</script>