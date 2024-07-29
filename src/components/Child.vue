<template>
    <h3>Child</h3>
    <p>{{ value }}</p>
    <p>{{ int }}</p>
    <ul>
        <li v-for="val, index of array" :key="index">{{ val }}</li>
    </ul>
    <p>{{ obj.name }}</p>
    <p>{{ obj.song }}</p>
</template>
<script>
export default{
    data(){
        return{

        }
    },
    props:["value","int","array","obj"]
}

</script>