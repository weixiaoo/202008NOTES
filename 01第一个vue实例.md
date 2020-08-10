##### 第一个Vue程序

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>第一个Vue程序</title>
    </head>
    <body>
        <!--1.将来new的Vue实例，会控制这个 元素中的所有内容-->
        <!--Vue实例所控制的这个元素区域，就是我们的 V-->

        <div id="app">
            {{ message }}
        </div>
        <!--1.导入Vue的包-->

        <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
        <script>
        //2.创建一个Vue实现
        //当我们导入包之后，在浏览器的内存中，就多了一个Vue构造函数
        //注意：我们new出来的这个 vm对象， 就是我们MVVM中的 VM调度者

            var app = new Vue({
               //表示，当前我们new的这个Vue实例，要控制页面上的哪个区域

                el:'#app', 
            //data属性中，存放的是el中要用到的数据
            //注意：这里的data就是MVVM中的M， 专门用来保存 每个页面的数据

                data:{
                    //通过Vue提供的指令，很方便的就能把数据渲染在页面中，程序员不再手动操作DOM元素了【前端的Vue之类的框架，不提倡我们去手动操作DOM元素了】

                    message:'Hello World!!'
                }
            })
        </script>
    </body>
</html>
```

```
1.v-cloak能够解决 插值表达式闪烁的问题
2.默认v-text是没有闪烁的问题的
3.v-text会覆盖元素中原本的内容，但是 插值表达式 只会替换自己的这个占位符，不会把 这个元素的内容清空
4.v-html能够识别data数据中的标签
5.v-bind：是Vue中，提供的用于绑定属性的指令
6.v-bind：指令可以简写为 :要绑定的属性 如 :title
7.v-bind中 可以写合法的JS表达式
8.Vue中提供了v-on:事件绑定机制
```

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>data数据对象</title>        

    </head>
    <body>    
        <div id="app">
            {{ message }}
            <h2> {{ school.name }} {{ school.mobile }} </h2>
            <ul>  
                <li>{{ campus[0] }}</li>
                <li>{{ campus[2] }} </li>
            </ul>
            <input type="button" value="按钮" v-on:click="show">
        </div>
        <!--开发环境版本， 包含了有帮助的命令行警告-->
        <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
        <script>
            //Vue中用到的数据定义在data中
            //data中可以写复杂类型的数据
            //渲染复杂类型数据市，遵守js的语法即可
            var app = new Vue({
                el:'#app',
                data:{
                    message:'黑马程序员',
                    school:{
                        name:'黑马程序员',
                        mobile:'123-123-456',                        
                    },
                    campus:['北京','广州','深圳','上海'],
                },
                methods:{
                    show:function() {
                        alert('ok?')
                    }
                }
            })
        </script>
    </body>
</html>
```

##### 小结

```
1.如何定义一个vue代码结构
2.插值表达式和 v-text
3.v-cloak
4.v-html
5.v-bind vue提供的属性绑定机制 缩写:
6.v-on   vue提供的事件绑定机制 缩写@
```
