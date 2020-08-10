##### v-if和v-show的使用

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
            <!-- <input type="button" value="toggle" @click="toggle"> -->
            <input type="button" value="toggle" @click="flag =! flag">

            <!-- v-if 的特点 每次都会重新删除或创建元素 -->
            <!-- v-show 的特点 每次不会重新进行DOM 的删除和创建操作 只是切换了元素的 display:none 样式 -->

            <!-- v-if 有较高的切换性能消耗 -->
            <!-- v-show 有较高的渲染消耗 -->

            <!-- 如果元素涉及到频繁的切换最好不要使用 v-if 而是使用v-show -->
            <!-- 如果元素可能永远也不会被显示出来被用户看到，则推荐使用 v-if -->
            <p v-if="flag">这是v-if控制的元素</p>
            <p v-show="flag">这是v-show控制的元素</p>
        </div>
    </body>
</html>
<script>
    //vue实例 得到ViewModel\
    var vm = new Vue({
        el:'#app',
        data:{
            flag:true,
        },
        methods:{
            /* toggle() {
                this.flag =! this.flag;
            } */
        },
    });
</script>
```
