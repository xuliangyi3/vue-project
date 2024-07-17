<template>
        -----------------------------
        <p>{{ msg }}</p>
    <div v-if=" word === 'A'">{{ word }}</div> 
    <div v-else-if=" word === 'B'">{{ word }}</div> 
    <div v-else-if=" word === 'C'">{{ word }}</div> 


    <div v-show="state">v-show {{ state }}</div>
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
            state:true,
            word:"B",

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
