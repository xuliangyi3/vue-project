<template>
    <!-- 对象绑定 -->
    <p :style="{ color:activeColor,fontsize:FontSize+'px' }">Style绑定1</p>
    <p :style="attr">Style绑定2</p>
</template>
<script>
export default {
    data() {
        return {
            activeColor:'red',
            FontSize:30,
            attr:{
                color:'green',
                fontsize:'100px'
            }
        
        }
    }
}
</script>
<style>

</style>