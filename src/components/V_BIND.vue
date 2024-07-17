<template>
    ----------------------------
    <p>{{ msg }}</p>
    <div v-bind="attr">{{ attr }}</div>
    <div :class="Class">v-bind</div>
</template>

<script>
export default {
    data() {
        return {
            msg: "动态绑定",
            attr: {
                id: "appID",
                class: "appClass"
            },
            Class:"appClass",
        }
    }
}
</script>
<style>
#appID{
   font-size: large;
}
.appClass{
    color: red;
}
</style>
