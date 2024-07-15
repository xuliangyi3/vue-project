<template>
    <div v-bind="attr" v-if="state">See</div>
</template>

<script>
export default {
    data() {
        return {
            msg: "条件渲染",
            attr: {
                // id: "appID",
                class: "appClass"
            },
            state:true
        }
    }
}
</script>
<style>
.appID{
    color: red;
}
.appClass{
    color: blue;
}
</style>
