<template>
    <h3>模板语法</h3>
    <p>{{ msg }}</p>
    <div v-bind:id="dynamicId" v-bind:class="dynamicClass">测试</div>
    <div v-bind="objectsOfAttrs">测试属性对象</div>
    <button :disabled="isButtonDisabled">按钮</button>
  </template>
  
  <script>
    export default {
      data(){
        return{
          msg: "神奇的语法",
          dynamicClass:"appclass",
          dynamicId:"appid",
          isButtonDisabled:true,
          objectsOfAttrs:{
            id:"appId",
            class:"appId"
          }    
        }
      }
    }
  </script>

<style>
.appclass{
  color:red;
  font-size: 30px;
}
</style>