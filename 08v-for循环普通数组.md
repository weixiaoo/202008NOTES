##### v-for循环普通数组

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
            <!-- <p>{{list[0]}}</p>
            <p>{{list[1]}}</p>
            <p>{{list[2]}}</p>
            <p>{{list[3]}}</p> -->
            <p v-for="(item,i) in list">索引值:{{i}} --- 每一项:{{item}}</p>
        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{
            list:[1,2,3,4,5,6]
        },
        methods:{},
    });
</script>    
```
