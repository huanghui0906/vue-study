<template>
    <div>
        <!--查询字符串列表-->
        <ul>
            <li v-for="(hero ,index) in heros" :key=index>
                {{hero.name}}
                <router-link :to="{name:'detail',query:{id:index}}">查看详情</router-link>
            </li>
        </ul>

    </div>
</template>

<script>
    export default {
        data(){
            return {
                heros:[{
                    name:'李白'
                },{
                    name:'王昭君'
                }]
            }
        }
    }
</script>

<style scoped>
ul{
    padding: 0;
    margin:0;
    padding-left: 20px;
}
    li{
        padding: 5px 0;
    }
</style>