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

```js
//第一种方法
function sum() {
            var a = prompt('输入数字a：');
            if (a == '') {
                alert('请输入值！');
                return;
            }
            var b = prompt('输入数字b：');
            if (b == '') {
                alert('请输入值！');
                return;
            }
            var sum = parseFloat(a) + parseFloat(b);
            console.log('两数的和为：' + sum);
        }
//第二种方法
        // arguments是伪数组 只有length属性
        var argFun = function(...arguments) {
            var sum = 0;
            for (var i = 0; i < arguments.length; i++) {
                sum += arguments[i];
            }
            return sum;
        }
//第三种方法
        var productArgs = (...arguments) => {
            var sum = 1;
            for (var i = 1; i < arguments.length; i++) {
                sum *= arguments[i];
            }
            return sum;
        }
```
# 产生随机数的函数
```js
// 返回了一个在指定值之间的随机数。这个值不小于 min（有可能等于），并且小于（不等于）max
        function  getRandom(min,  max)  {   
            return  Math.floor(Math.random()  * (max  - min +  1))  +  min; 
        }

        // 返回了一个在指定值之间的随机数。包含min和max
        function getRandomIntInclusive(min, max) {
            min = Math.ceil(min);
            max = Math.floor(max);
            return Math.floor(Math.random() * (max - min + 1)) + min; //含最大值，含最小值 
        }
```

# 闰年计算
```js
var score = parseInt(prompt('输入学生成绩：'));
        if (score >= 90 && score <= 100) {
            console.log('优秀');
        } else if (score >= 80) {
            console.log('良好');
        } else if (score >= 70) {
            console.log('一般');
        } else if (score >= 60) {
            console.log('及格');
        } else {
            console.log('不及格');
        }
        let _31 = 31;
        let _30 = 30;
        let _29 = 29;
        let _28 = 28;
        var monthday = parseInt(prompt('输入月份：'));
        do {
            switch (monthday) {
                case 1:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                case 2:
                    let year = parseInt(prompt('请输入年份：'));
                    if (year % 4 == 0 && year % 400 == 0 || year % 100 != 0) {
                        console.log(year + '为闰年');
                        console.log(monthday + '月有' + _29 + '天');
                    } else {
                        console.log(year + '为平年');
                        console.log(monthday + '月有' + _28 + '天');
                    }
                    break;
                case 3:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                case 4:
                    console.log(monthday + '月有' + _30 + '天');
                    break;
                case 5:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                case 6:
                    console.log(monthday + '月有' + _30 + '天');
                    break;
                case 7:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                case 8:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                case 9:
                    console.log(monthday + '月有' + _30 + '天');
                    break;
                case 10:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                case 11:
                    console.log(monthday + '月有' + _30 + '天');
                    break;
                case 12:
                    console.log(monthday + '月有' + _31 + '天');
                    break;
                default:
                    console.log('输入格式错误');
            }
            monthday = parseInt(prompt('输入月份：'));
        } while (monthday > 0 && monthday <= 12);
```