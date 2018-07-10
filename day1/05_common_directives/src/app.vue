<template>
    <!-- 只能有1个根节点 -->
    <div>
         <pre>
                * v-text 是元素的innerText只能在双标签中使用
                * v-html 是元素的innerHTML，不能包含<!-- {{xxx}} -->
                * v-if 元素是否移除或者插入
                * v-show 元素是否显示或隐藏
                * v-model
        </pre>
        v-text :
        <span v-text="text"></span>
        <input type="text" v-text="text">
        <br/>
        v-html:
        <span v-html="html"></span>
        v-if:
        <span v-if="isShow">为true的话。我会显示-----hello，远方的朋友还好吗？</span>
    </div>
</template>

<script>
    export default {
      data(){
          return{
              text:"大家好",
              html:`
                    <ui>
                         <li>jake</li>
                         <li>jake2</li>
                         <li>jake3</li>
                         <li>jake4</li>
                         <li>jake4</li>
                         <li>jake4</li>
                         <li>jake4</li>
                         <li>jake4</li>
                         <li>不能包含这个{{text}}</li>
                    </ui>
                    `
              ,
              isShow:true
          }
      }
    }
</script>

<style scoped>

</style>