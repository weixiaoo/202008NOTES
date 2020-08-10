##### v-for迭代数字

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
            <!-- in后面 可以加普通数组 对象数组 对象 还可以加数字 -->
            <!-- 注意：如果使用 v-for 迭代数字的话 前面的 count 值从1 开始 -->
            <p v-for="count in 10">这是第 + {{count}} + 次循环</p>
        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{},
        methods:{},
    });
</script>
```
