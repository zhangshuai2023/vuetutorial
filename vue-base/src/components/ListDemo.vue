<template>
    <h3>列表渲染</h3>
    <p v-for="(item,index) in names" :key="index">{{ item }}-{{ index }}</p>
    <div v-for="item in result">
        <p>{{ item.title }}</p>
        <img v-bind:src="item.avator" alt="" />
    </div>
    <div v-for="(value, key, index) in userInfo">
        <p>{{ value }}-{{ key }}-{{ index }}</p>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                names:["项目1","项目2","项目3"],
                result:[
                    {
                        "id":2261677,
                        "title":"鄂尔多斯|感受一座城市的璀璨夜景感受一座城市，除了白日里的车水马龙",
                        "avator":"https://pic.qyer.com/avatar/002/25/77/30/200?v=1560226451",
                    },
                    {
                        "id":2261566,
                        "title":"成都这家洞穴暗黑风咖啡厅酷毙了口早C晚A走起急成都天气这么热咖啡米人必",
                        "avator":"https://pic.qyer.com/avatar/011/07/08/69/200?v=1572185180",
                    },
                    {
                        "id":2261662,
                        "title":"[川西新龙-措卡湖]措卡湖，意为“乱石丛中的黑色海水”，神秘小众原汁原味。",
                        "avator":"https://pic.qyer.com/avatar/009/88/48/58/200?v=1507386782",
                    }
                ],
                userInfo:{
                    name:"Iwen",
                    age:20,
                    sex:"male"
                }
            }
        }
    }
</script>