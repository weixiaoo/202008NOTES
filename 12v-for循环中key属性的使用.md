##### v-for循环中key属性的使用

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <script src="../lib/vue.min.js"></script>
    </head>
    <body>
        <div id="app">

            <div>
                <label>Id:
                    <input type="text" v-model="id">
                </label>
                <label>Name:
                    <input type="text" v-model="name">
                </label>
                <label>
                    <input type="button" value="添加" @click="add">
                </label>
            </div>

            <!-- 注意：v-for 循环的时候 key 属性只能使用 number 获取 属性 -->
            <!-- 注意：key 在使用的时候 必须使用 v-bind 属性绑定的形式 指定 key 的值 -->
            <!-- 在组件中，使用 v-for 循环的时候， 或者在一些特殊情况中，如果 v-for 有问题， 必须在使用 v-for 的同时， 指定唯一的 字符串/数字 类型 :key 值 -->
            <p v-for="item in list" :key='item.id'>
                <input type="checkbox">
                {{item.id}} --- {{item.name}}
            </p>

        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{
            id:'',
            name:'',
            list:[
                {id:1,name:'李斯'},
                {id:2,name:'嬴政'},
                {id:3,name:'赵高'},
                {id:4,name:'韩非'},
                {id:5,name:'荀子'}
            ]
        },
        methods:{
            add() { 
                //尾部添加方法
                // this.list.push({id:this.id,name:this.name})

                //头部添加方法
                this.list.unshift({id:this.id,name:this.name})
            }
        },
    });
</script>
```
