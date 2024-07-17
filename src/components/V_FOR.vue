<template>
    ---------------------------
    <div v-bind:class="attr">msg</div>
    <p v-for="name,index of names">{{ name }}--{{ index }}</p>

    <p v-for="value,key,index of userInfo">{{ key }}---{{ value }}---{{ index }}</p>

    <div v-for="result in results" :key="result.id">
        <p>{{ result.id }},{{ result.title }}</p>
        <img :src="result.src">
    </div>
</template>

<script>
export default {
    data() {
        return {
            msg: "列表渲染",
            attr: "appClass",
            names: ["多读书", "多看报", "少吃零食", "多睡觉"],
            results: [
                {
                    "id": 1,
                    "title": "苹果",
                    "src": "https://ts4.cn.mm.bing.net/th?id=OIP-C.HTN-sUDdcgATz6BiZn5yeQHaH7&w=241&h=258&c=8&rs=1&qlt=90&o=6&dpr=1.3&pid=3.1&rm=2",
                },
                {
                    "id": 2,
                    "title": "西瓜",
                    "src": "https://ts2.cn.mm.bing.net/th?id=OIP-C.INxfvqUVwIgan0pfwFrbXgHaHa&w=250&h=250&c=8&rs=1&qlt=90&o=6&dpr=1.3&pid=3.1&rm=2",
                },
                {
                    "id": 3,
                    "title": "香蕉",
                    "src": "https://ts2.cn.mm.bing.net/th?id=OIP-C.JIE9eUSxFmiw15Du2ZC-XAHaGJ&w=274&h=227&c=8&rs=1&qlt=90&o=6&dpr=1.3&pid=3.1&rm=2"
                }

            ],
            userInfo:{
                name:"xuliangyi",
                age:19,
                sex:"male"
            }
        }
    }
}
</script>
<style>
.appID {
    color: red;
}

.appClass {
    color: blue;
}
</style>
