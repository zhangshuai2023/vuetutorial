<template>
    <h3>内联事件处理</h3>
    <button v-on:click="count++">Add</button>
    <p>{{ count }}</p>
    <h3>方法事件处理</h3>
    <button v-on:click="addCount('hello', $event)">Add2</button>
    <p>count is: {{ count }}</p>
    <h3>事件传参</h3>
    <p @click="getNameHandler(item)" v-for="(item, index) in names" :key="index">{{ item }}</p>
    <h3>事件修饰符</h3>
    <a @click.prevent="clickHandler" href="https://cn.vuejs.org/">这是一个网址Vue官网</a>

</template>

<script>
    export default{
        data(){
            return{
                count:0,
                names:["iwen","ime","frank"]
            }
        },
        //所有方法或者函数都在这里
        methods:{
            addCount(msg,e){
                this.count+=1;
                console.log("点击啦");
                //获取一个 event 对象, vue 中 event 对象就是 原生 JS event对象
                console.log(e.target);
                e.target.innerHTML = "Add" + this.count;
                //传递参数
                console.log(msg);
            },
            //点谁获取谁
            getNameHandler(name){
                console.log(name);
            },
            clickHandler(e){
                //通过 event 对象阻止默认事件
                //e.preventDefault();
                console.log("请不要试图访问");
            }
        }
    }
</script>