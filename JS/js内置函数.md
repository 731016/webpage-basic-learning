```js
<script>
        var obj = new Object();
        obj.name = '胡梓卓';
        // obj.constructor.sing = function() {
        //     console.log('223');
        // }

        console.dir(obj);
        console.log(obj.hasOwnProperty('name'));
        console.log(obj.toString());
        console.log(this);
        console.log(Math.PI);
        console.log(Math.random());
        // 向下取整 比他小
        console.log(Math.floor(1.5));
        console.log(Math.floor(1.4));
        console.log(Math.floor(1.6));
        console.log(Math.floor(-1.5));
        console.log(Math.floor(-1.4));
        console.log(Math.floor(-1.6));
        // 向上取整 比他大
        console.log(Math.ceil(1.4));
        console.log(Math.ceil(1.5));
        console.log(Math.ceil(1.6));
        console.log(Math.ceil(-1.4));
        console.log(Math.ceil(-1.5));
        console.log(Math.ceil(-1.6));
    </script>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/121447_e62f4454_8254421.png "js.png")

# 函数-累加求和
```js
<script>
        function printSingle() {
            document.write('△');
        }
        // printSingle();
        function sum(num) {
            let sum = 0;
            for (let i = 0; i < num; i++) {
                sum += i;
            }
            document.write('<h2 style="color:#FC011A;">' + sum + '</h2>');
            // console.log(sum);
        }
        sum(prompt('输入要累加的数：'));
    </script>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/124820_122e15ba_8254421.png "sum.png")