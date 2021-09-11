```html
<body>
    <input type="checkbox" name="" id="choose" value="全选">全选/全不选
    <input type="checkbox" name="" id="" value="1">1
    <input type="checkbox" name="" id="" value="2">2
    <input type="checkbox" name="" id="" value="3">3
    <input type="checkbox" name="" id="" value="4">4
    <input type="checkbox" name="" id="" value="5">5

    <input type="button" value="追加标签" id="add">
    <input type="button" value="清空标签" id="del">
    <div class="content"></div>
    <script>
        var input = document.getElementsByTagName('input');
        input[0].onclick = function() {
            for (let i = 0; i < input.length; i++) {
                input[i].checked = this.checked;
            }
            // if (this.checked == true) {
            //     for (let i = 0; i < input.length; i++) {
            //         input[i].checked = true;
            //     }
            // } else {
            //     for (let i = 0; i < input.length; i++) {
            //         input[i].checked = false;
            //     }
            // }
        }

        var add = document.getElementById('add');



        add.onclick = function() {
            var h1 = document.createElement('h1');
            h1.innerText = '一个苹果';
            var content = document.getElementsByClassName('content')[0];
            content.appendChild(h1);

            // for (let i = 0; i < content.childNodes.length; i++) {
            // }
        };
        var del = document.getElementById('del');
        del.onclick = function() {
            var content = document.getElementsByClassName('content')[0];
            content.remove();
        };
    </script>
</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/115855_5f39b122_8254421.png "date.png")

# 计算从出生到现在自己出生了多少天，定时器
```js
<script>
        function DateTime() {
            let date = new Date();
            let year = date.getFullYear();
            let month = date.getMonth() + 1; // [0-11]
            let day = date.getDate();
            let hour = date.getHours();
            let minutes = date.getMinutes();
            let senconds = date.getSeconds();
            return year + '年' + month + '月' + day + '日' + hour + '时' + minutes + '分' + senconds + '秒';
        }
        // var date = new Date();
        // console.log(DateTime());
        // let day = date.getDay(); //一周第几天
        // let millisecond = date.getTime(); // 获取当前时间的毫秒值
        // console.log(day);
        // console.log(millisecond);
        // let localTime = date.toLocaleDateString(); //获取本机时间
        // console.log(localTime);
        // let localdate = date.toLocaleTimeString(); //获取本机日期
        // console.log(localdate);
        // console.log(date.toLocaleString());

        function setDateTime(birday) {
            let bti = parseInt((new Date(birday).getTime()) / 1000 / 60 / 60 / 24);
            let now = parseInt(Date.now() / 1000 / 60 / 60 / 24);
            return now - bti + '天';
        }
        console.log(setDateTime('2000/1/11'));
        var setime = setTimeout(function() {
            console.log('炸弹定时器');
        }, 1000);
        clearTimeout(setime);
        var setInterval = setInterval(() => {
            clearInterval(setInterval);
            console.log('闹钟定时器');
        }, 1000);
    </script>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/120440_cea8735a_8254421.png "bir.png")