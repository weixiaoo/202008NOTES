##### Vue中的样式-style

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
            <!-- 对象就是无序键值对的集合 -->
            <!-- <h1 :style="{color:'red','font-weight':200}">这是一个h1</h1> -->

            <!-- <h1 :style="styleObj1">这是一个h1</h1> -->

            <h1 :style="[styleObj1, styleObj2]">这是一个h1</h1>
        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{
            styleObj1:{color:'red','font-weight':200},
            styleObj2:{'font-style':'italic'},
        },
        methods:{},
    });
</script>
```
