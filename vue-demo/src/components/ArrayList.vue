<template>
    <h3>数组变化侦听</h3>
    <button @click="addListHandler">添加数据</button>
    <ul>
        <li v-for="(name,index) in names" :key="index">{{name}}</li>
    </ul>
</template>

<script>
    export default{
        data(){
            return{
                names:['张三','李四','王五'],
            }
        },
        methods:{
            addListHandler(){
                // UI 自动更新的方法
                this.names.push('赵六');
                // UI 不会自动更新的方法
                this.names.concat('赵六');
                // 要更新数组，进行浅拷贝
                this.names=this.names.concat('赵六');
            }
        }
    }
</script>