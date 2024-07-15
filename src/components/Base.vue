<template>
    <h3>模板语法</h3>
    <p>{{ msg }}</p>
    <p>{{ ok ? "ture" : "false" }}</p>
    <p>{{ Hello.split("").reverse().join("") }}</p>
    <p v-html="baidu"></p>
    <p v-bind="attr"> {{ attr }}</p>
  </template>
  
  <script>
  export default {
    data() {
      return {
        msg: "Demo",
        ok: true,
        Hello: "dlruoW olleH",
        baidu: "<a href='https://www.baidu.com' target='_blank'>百度</a>",
        attr: {
          id: "appid",
          class: "appclass"
        }
      }
    }
  }
  </script>
  
  <style>
  .appid {
    color: red;
    font-size: 20rpm;
  }
  
  .appclass {
    color: blue;
    font-size: 20rpm;
  }
  </style>