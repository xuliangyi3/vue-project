<template>
    <p>{{ msg }}</p>
    <p>{{ calcuationFavorite }}</p>
</template>
<script>
export default {
    data() {
        return {
            msg: "计算属性",
            attr: {
                name: "xulaingyi",
                age: 19,
                favorite: ['西瓜', '香蕉', '苹果']
            }
        }
    },
    // 计算属性
    computed: {
        calcuationFavorite() {
            console.log(this.attr)
            return this.attr.favorite.length > 0 ? 'yes' : 'NO'
        }
    }
}
</script>