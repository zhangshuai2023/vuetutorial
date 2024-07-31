<template>
    <h3>计算属性</h3>
    <h3>{{ company.name }}</h3>
    <p>{{ company.address.length>0 ? 'Yes':'No' }}</p>
    <p>{{ addressLength }}</p>

</template>

<script>
    export default{
        data(){
            return{
                company:{
                    name:'腾讯',
                    address:['北京','上海','广州','深圳']
                }
                
            }
        },
        // 计算属性
        computed:{
            // 获取数组的长度
            addressLength(){
                return this.company.address.length;
            }
        },
        // 计算属性和方法的区别
        methods:{
            changeAddress(){
                this.company.address.push('杭州');
            }
        }
    }

</script>