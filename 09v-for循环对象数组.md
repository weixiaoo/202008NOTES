##### v-for循环对象数组

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
            <p v-for="(user,i) in list"> {{user.id}} --- 名字:{{user.name}} --- 索引:{{i}}</p>
        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{
            list:[{id:1,name:'zs'},
            {id:2,name:'li'},
            {id:3,name:'ww'},
            {id:4,name:'ll'}]
        },
        methods:{},
    });
</script>
```
