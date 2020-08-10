##### v-for循环对象

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
            <!-- 注意：在遍历对象身上的键值对的时候，除了有 val key ，在第三个位置还有 一个 索引 -->
            <p v-for="(val,key,i) in user">
                值是:{{val}} --- 键是:{{key}} --- 索引:{{i}}
            </p>
        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{
            user:{
                id:1,
                name:'张三',
                gender:'男',
            }
        },
        methods:{},
    });
</script>
```
