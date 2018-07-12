<template>
    <div>
      <!--   请输入内容：
        <input type="text" v-model="text">
        <br/>
        显示：{{text | myFilter}}
        <br>-->
        <sub-vue></sub-vue>
    </div>
</template>

<script>
    import subVue from "./component/subVue.vue"
    export default {
        name: "app",
        filters:{
            myFilter:function (value) {
                console.log(value);

                return value.split('').reverse().join('');
            }
        },
        data(){
            return{
                text:'',

            }
        },
        components:{
            subVue:subVue
        }
    }
</script>

<style scoped>

</style>