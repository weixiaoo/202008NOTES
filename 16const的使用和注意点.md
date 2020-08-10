##### const的使用

```
1.const关键字
在很多语言中已经存在，比如c、c++中，主要的作用是将某个变量修饰为常量
在JavaScript中也是如此，使用const修饰的标识符为常量，不可以再次赋值
```

```
2.什么时候使用const
当我们修饰的标识符不会被再赋值时，就可以使用const来保证数据的安全性
```

```
建议：
在开发中优先使用const，只有需要改变某个标识符的时候才使用let
```

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>title</title>
    </head>
    <body>
        <script type="text/javascript">
            // 1.注意一:const修饰的标识符被赋值后,不能再修改
            // const name = 'why';
            // name = 'hao';

            // 2.注意二:const定义标识符的时候 必须赋值
            // const name;

            // 3.注意三:常量的含义是指向对象的时候不能被修改,但是可以改变对象内部的属性
            const obj = {
                name:'why',
                age: 18,
                height:180,
            }
            obj.name = 'hao';
            obj.age = 20;
        </script>
    </body>
</html>
```
