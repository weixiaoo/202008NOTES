##### Vue中的样式-class

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <script src="../lib/vue.min.js"></script>
        <style>
            .red {
                color: #00008B;;
            }
            .thin {
                font-weight: 200;
            }
            .italic {
                font-style: italic;
            }
            .active {
                letter-spacing: 0.5em;
            }
        </style>
    </head>
    <body>
        <div id="app">
            <!-- <h1 class="red thin">这是一个很大的div!!!</h1> -->

            <!-- 第一种使用方式，直接传递一个数组，注意：这里的class需要使用 v-bind 做数据绑定 -->
            <!-- <h1 :class="['red','thin','italic']">这是一个很大的div!!!</h1> -->

            <!-- 在数组中使用三元表达式 -->
            <!-- <h1 :class="['red','thin',flag?'active':'']">这是一个很大的div!!!</h1> -->

            <!-- 在数组中使用 对象来代替三元表达式  提高代码的可读性 -->
            <!-- <h1 :class="['red','thin',{active:flag}]">这是一个很大的div!!!</h1> -->

            <!-- 在为 class 使用 v-bind 绑定 对象的时候，对象的属性是类名，对象的属性可带引号 也可不带引号 属性的值 是一个标志符 -->
            <h1 :class="classObj">这是一个很大的div!!!</h1>
        </div>
    </body>
</html>
<script>
    //创建vue实例 得到ViewModel
    var vm = new Vue({
        el:'#app',
        data:{
            flag:false,
            classObj:{ red:true, thin:true, italic:false, active:false, },
        },
        methods:{},
    });
</script>
```
