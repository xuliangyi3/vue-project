<template>
    <form>
        <input type="text"  v-model="msg">
        <p>{{ msg }}</p>
        <input type='checkbox' id="checkbox" v-model="checked">
        <label for='checkbox' >{{ checked }}</label>
    </form>
</template>
<script>
export default{
    data(){
        return{
            msg:"",
            checked:false
        }
    }
}
</script>