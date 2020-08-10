##### v-on的参数传递问题

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>title</title>
    </head>
    <body>
        <div id="app">
            <button type="button" @click="btn1Click()">按钮1</button>
            <button type="button" @click="btn1Click">按钮1</button>
            <!-- 1.在事件定义时，写函数时省略了小括号，但是方法本身是需要传递一个参数的 -->

            <button type="button" @click="btn2Click(123)">按钮2</button>
            <!-- 2.如果函数需要参数 但是没有传入 那么函数的形参为undefind -->

            <button type="button" @click="btn2Click()">按钮2</button>
            <!-- event -->
            <button type="button" @click="btn3Click">按钮3</button>
            <!-- 3.方法定义时，需要event对象，同时又需要其他参数 需要$event传入事件-->

            <!-- <button type="button" @click="btn4Click(abc,event)">按钮4</button> -->
            <button type="button" @click="btn4Click(123,$event)">按钮4</button>            

        </div>
        <script src="../lib/vue.min.js" type="text/javascript" charset="utf-8"></script>
        <script type="text/javascript">
            const app = new Vue({
                el:'#app',
                data: {
                    message:'你好？',
                    // abc: 123,
                    // event:'codewhy',
                },
                methods: {
                    btn1Click() {
                        console.log(this.message)
                    },
                    btn2Click(abc) {
                        console.log('----',abc)
                    },
                    btn3Click(event) {
                        console.log('----',event)
                    },
                    btn4Click(abc,event) {
                        console.log('++++',abc,event)
                    }
                }
            })
        </script>
    </body>
</html>
```
