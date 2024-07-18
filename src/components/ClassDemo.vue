<template>
    <!-- 对象绑定 -->
    <p :class="{ 'active': isActive, 'text-danger': hasError }">Class样式绑定1</p>
    <!-- 多个对象绑定 -->
    <p :class="attr">Class样式绑定2</p>
    <!-- 数组绑定 -->
    <p :class="[arrDanger, arrActive]">Class样式绑定3</p>
    <p :class="[isActive ? 'active text-danger' : '']">Class样式绑定4</p>
    <!-- 数组和对象绑定 -->
    <!-- 数组和对象嵌套过程中,只能是数组嵌套对象 -->
    <p :class="[{ 'active': isActive, 'text-danger': hasError }]">Class样式绑定5</p>
    <p :class="[isActive ? 'active' : '',{'text-danger': hasError }]">Class样式绑定6</p>

</template>
<script>
export default {
    data() {
        return {
            isActive: true,
            hasError: true,
            attr: {
                'active': true,
                'text-danger': true,
            },
            arrActive: 'active',
            arrDanger: 'text-danger'
        }
    }
}

</script>
<style>
.active {
    font-size: large;
}

.text-danger {
    color: red;
}
</style>