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

# 字符串函数
```js
<script>
        // var str = new String('html');
        // console.log(str.length); // 字符长度
        // console.log(str.charAt(2)); // 返回指定位置的字符 参数为下标
        // console.log(str.charCodeAt(2)); // 返回指定字符的unicode编码 参数下标
        // console.log(str.concat('123456')); // 连接字符串
        // console.log(str.slice(1, 3)); // 根据下标 返回字符串 包含前一个下标，不包含后一个下标
        // console.log(str.substring(1, 3)); //  返回两个索引号之间的字符 包含前一个下标，不包含后一个下标
        // console.log(str.substr(1, 1)); // 从第一个参数开始截取，后一个参数为要截取的长度
        // console.log(str.indexOf('t')); // (从前往后)根据字符找到下标，未找到返回-1
        // console.log(str.lastIndexOf('r')); // (从后往前)根据字符找到下标，未找到返回-1
        // console.log(str.trim()); // 删除字符串两端空格
        // console.log(str.toUpperCase()); //转大写
        // console.log(str.toLowerCase()); // 转小写
        // console.log(str.split('t')); //分割字符串数组
        // console.log(str.split('t')[0]); //分割字符串数组
        // console.log(str.split('t')[1]); //分割字符串数组
        // for (let i = 0; i < str.length; i++) {
        //     console.log(str[i]);
        // }
        var str = 'asdfghjkl';
        var strArr = [];
        // for (let i = 97; i <= 122; i++) {
        //     for (let j = 0; j < str.length; j++) {
        //         if (i == str.charCodeAt(j)) {
        //             strArr[length++] = str[j];
        //         }
        //     }
        // }
        // let newStr = strArr.toString();
        // for (let i = 0; i < newStr.length; i++) {
        //     newStr = newStr.replace(',', '');
        // }
        // console.log(newStr);
        for (let i = 0; i < str.length; i++) {
            for (let j = 0; j < str.length - 1; j++) {
                if (str.charCodeAt(j) > str.charCodeAt(j + 1)) {
                    strArr[length++] = str[j + 1];
                }
            }
        }
        console.log(strArr);
    </script>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/131600_f83d39ce_8254421.png "str.png")

# 打印素数，三角形，表达式的值
> ___*    1   1
> __***   2   3
> _*****  3   5
> ******* 4   7

> 素数 只能被1和自身整除的数
> 101-200

> 1-2 +3-4 + 5-...+n


> 顺序输出1~100
> 3 T
> 5 F
> 15 TF
```js
<script>
        //输入行数，打印三角形
        function triangle(rowCount) {
            rowCount = parseInt(rowCount);
            for (let i = 1; i <= rowCount; i++) {
                for (let x = rowCount - i - 1; x >= 0; x--) {
                    // console.log('x=' +x);
                    document.write('&nbsp;');
                }
                for (let y = 1; y <= 2 * i - 1; y++) {
                    // console.log('y=' + y);
                    document.write('<span style="font-weight:700">*</span>');
                }
                document.write('<br>');
            }
        }
        // triangle(10);

        //打印指定范围内的素数
        function primrNumber(mix, max) {
            for (let i = mix; i <= max; i++) {
                let flag = true;
                for (let j = 2; j < i; j++) {
                    if (i % j == 0) {
                        flag = false;
                        break;
                    }
                }
                if (flag) {
                    document.writeln(i);
                }
            }
        }
        primrNumber(1, 100);

        //计算表达式1-2+3-4+5-6+...+n的值
        function cal(n) {
            n = parseInt(n);
            let sum = 0;
            for (let i = 1; i <= n; i++) {
                let num = i;
                if (i % 2 == 0) {
                    num = (-1) * i;
                }
                sum += num;
            }
            document.write(sum);
            // console.log(sum);
        }
        cal(prompt('请输入n的值：'));

        function sequence() {
            for (let i = 1; i <= 100; i++) {
                document.writeln(i);
                if (i % 3 == 0 && i % 5 == 0) {
                    document.writeln('TF' + '<br>');
                    continue;
                }
                if (i % 3 == 0) {
                    document.writeln('T<br>');
                } else if (i % 5 == 0) {
                    document.writeln('F<br>');
                } else {
                    document.write('<br />');
                }

            }
        }
        // sequence();
    </script>
```
> 统计字母，数字，特殊字符；\
> 判断是否为整数；\
> 4位数 前2位和后两位相等 且4位数能开方；\
> 输入年份得到二月天数
```js
<script>
        // 1.统计字母，数字，特殊字符
        function count(str) {
            str = str.trim();
            let letter = 0,
                number = 0,
                specchar = 0;
            for (let i = 0; i < str.length; i++) {
                //if(str[i]>='a' && str[i]<='z'){}else if(str[i]>='A'&&str[i]<='Z'){}
                if (str.charCodeAt(i) >= 97 && str.charCodeAt(i) <= 122) {
                    letter++;
                    // else if(str[i]>='0'&&str[i]<='9'){}
                } else if (str.charCodeAt(i) >= 48 && str.charCodeAt(i) <= 54) {
                    number++;
                } else {
                    specchar++;
                }
            }
            return '英文字符：' + letter + '数字：' + number + '特殊字符：' + specchar;
        };
        // var str = prompt('请输入要统计的字符串：');
        // var amount = count(str)
        // document.write('<h2>' + amount + '</h2>');

        //2.判断是否为整数
        function isInteger(num) {
            num = Math.sqrt(num);
            let str = num + '';
            if (str.indexOf('.') == -1) {
                return true;
            } else {
                return false;
            }
        }

        //3. 4位数 前2位和后两位相等 且4位数能开方
        function fourFigures() {
            let arr_4 = [];
            for (let i = 1000; i <= 9999; i++) {
                // let kilobit = parent(i / 1000) ;
                // let hundreds = parent(i / 100 % 10);
                // let decade = parent(i / 10 % 10);
                // let unit = parent(i % 10);
                let beforeNum = parseInt(i / 100);
                let afterNum = i % 100;
                // i==Math.sqrt(i)
                if (isInteger(i) && beforeNum == afterNum) {
                    arr_4[length++] = i;
                    console.log(i);
                }
            }
            console.log(arr_4);
        };
        fourFigures();

        //4. 输入年份得到二月天数
        function getFebruaryDay(day) {
            if (day % 4 == 0 && day % 100 != 0 || day % 400 == 0) {
                document.writeln(day + '是闰年，二月有29天' + '<br>');
            } else {
                document.writeln(day + '是平年，二月有28天' + '<br>');
            }
        }
        // getFebruaryDay(2020);
        // getFebruaryDay(1900);
        // 输入年份得到二月天数
        function acquireFebruaryDay(year) {
            var date1 = new Date(year + '/02/01');
            var date2 = new Date(year + '/03/01');
            var time1 = date1.getTime();
            var time2 = date2.getTime();
            console.log((time2 - time1) / 1000 / 60 / 60 / 24 + '天');
        }
        acquireFebruaryDay(2008);
    </script>
```