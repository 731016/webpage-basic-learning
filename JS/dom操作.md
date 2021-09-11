```html
<body>
    <p id="title">打分法</p>
    <input type="text" value="123" name="username">
    <a href="#">超链接</a>
    <p class="con">后哦阿胶高哦电话费㐎</p>

    <input type="button" value="创建标签">
    <div class="box"></div>
    <script>
        document.write('<h2>通过文档对象书写标签</h2>');
        document.writeln('通过文档对象书写标签,加空格');
        console.log(document.getElementById('title')); //通过ID获取标签
        // document.getElementsByClassName('类名');
        console.log(document.getElementsByName('username')); // 通过name获取,返回节点列表,类型为伪数组
        console.log(document.getElementsByTagName('a')); //根据标签名称返回html集合
        console.log(document.getElementsByClassName('con')); //根据类名返回html集合
        var btn = document.getElementsByTagName('input')[1];

        btn.onclick = function() {
            var box = document.getElementsByClassName('box')[0];
            box.innerHTML = '<h2>都去的话</h2>';
        }
    </script>
</body>
```
**效果展示**<br>
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/124529_d609c19a_8254421.png "dom.png")

# dom操作-改变背景颜色
```html
<body>
    <!-- <input type="button" value="点击按钮">
    <input type="text" name="" id=""> -->
    <div class="box">
        <input type="button" value="红色">
        <input type="button" value="蓝色">
        <input type="button" value="绿色">
    </div>
    <select name="" id="select">
        <option value="">请选择城市</option>
        <option value="1">武汉</option>
        <option value="2">上海</option>
        <option value="3">广州</option>
        <option value="4">重庆</option>
    </select>
    <script>
        var btn = document.getElementsByTagName('input');
        // btn[0].onclick = function() {
        //     console.log('触发点击事件');
        // }
        // btn[1].onfocus = function() {
        //     this.value = '获得焦点';
        // }
        // btn[1].onblur = function() {
        //     this.value = '失去焦点';
        // }
        btn[0].onclick = function() {
            // this.parentElement.setAttribute('backgroundColor', 'red');
            this.parentElement.style.backgroundColor = 'red';
        };
        btn[1].onclick = function() {
            this.parentElement.style.backgroundColor = 'blue';
        };
        btn[2].onclick = function() {
            this.parentElement.style.backgroundColor = 'green';
        };
        // 立即执行函数
        // (function() {
        //     alert(1)
        // })();
        // (function() {
        //     alert(2)
        // }());
        document.getElementsByClassName('box')[0].onmouseenter = function() {
            console.log(1);
        };
        //移动到子元素也会触发 会冒泡
        // document.getElementsByClassName('box')[0].onmouseover = function() {
        //     console.log(2);
        // };
        var select = document.getElementById('select');
        select.onchange = function() {
            console.log(this.value);
        }
    </script>
</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/130511_2a1e46c8_8254421.png "color.png")

# dom操作-添加和删除节点
```html
<body>
    <div class="box">
        <input type="button" value="添加" id="add">
        <input type="button" value="删除" id="del">
        <table border="1" cellspacing="0" cellpadding="0">
            <tr>
                <th></th>
                <th>姓名</th>
                <th>年龄</th>
                <th>部门</th>
                <th>操作</th>
            </tr>
            <tr>
                <td><input type="checkbox" name="" id="" class="choose"></td>
                <td>张三</td>
                <td>34</td>
                <td>财务部</td>
                <td><a href="javascript:;">删除</a></td>
            </tr>
            <tr>
                <td><input type="checkbox" name="" id="" class="choose"></td>
                <td>李四</td>
                <td>34</td>
                <td>财务部</td>
                <td><a href="javascript:;">删除</a></td>
            </tr>

        </table>
    </div>
    <script>
        function getRandSum(min, max) {
            return parseInt(Math.random() * (max - min + 1) + min);
        }
        document.onclick = function(e) {
                if (e.target.value == '添加') {
                    var tbody = document.getElementsByTagName('tbody')[0];
                    var newtr = document.createElement('tr');
                    // var newtrAccomplish = tbody.appendChild(newtr);
                    var newtrAccomplish = tbody.insertAdjacentElement("beforeend", newtr);
                    //生成tr td标签
                    for (let i = 0; i < 5; i++) {
                        if (i == 0) {
                            var newtd = document.createElement('td');
                            newtrAccomplish.appendChild(newtd).innerHTML = '<input type="checkbox" name="" id="" class="choose">';
                        } else if (i == 4) {
                            // var newtd = document.createElement('td');
                            // newtrAccomplish.appendChild(newtd).innerHTML = '<a href="javascript:;">删除</a>';
                            newtrAccomplish.insertAdjacentHTML("beforeend", '<td><a href="javascript:;">删除</a></td>');

                        } else {
                            var newtd = document.createElement('td');
                            newtrAccomplish.appendChild(newtd).innerText = getRandSum(20, 70);
                        }
                    }
                } else if (e.target.value == '删除') {
                    var inputChoose = document.getElementsByClassName('choose');
                    var table = document.getElementsByTagName('table');
                    for (let i = 0; i < inputChoose.length; i++) {
                        if (inputChoose[i].checked == true) {
                            inputChoose[i].parentNode.parentNode.remove();
                            i--;
                        }
                    }
                } else if (e.target.href == 'javascript:;') {
                    e.target.parentNode.parentNode.remove();
                }
            }
            // var add = document.getElementById('add');
            // var del = document.getElementById('del');
            // // 添加按钮
            // add.onclick = function() {
            //     var tbody = document.getElementsByTagName('tbody')[0];
            //     var newtr = document.createElement('tr');
            //     var newtrAccomplish = tbody.appendChild(newtr);
            //     //生成tr td标签
            //     for (let i = 0; i < 5; i++) {
            //         if (i == 0) {
            //             var newtd = document.createElement('td');
            //             newtrAccomplish.appendChild(newtd).innerHTML = '<input type="checkbox" name="" id="" class="choose">';
            //         } else if (i == 4) {
            //             var newtd = document.createElement('td');
            //             newtrAccomplish.appendChild(newtd).innerHTML = '<a href="javascript:;">删除</a>';
            //         } else {
            //             var newtd = document.createElement('td');
            //             newtrAccomplish.appendChild(newtd).innerText = getRandSum(20, 70);
            //         }
            //     }

        //     // 给新生成的最后的一个tr标签里面的最后一个td标签里面的a标签绑定点击事件
        //     var tr = document.getElementsByTagName('tr');
        //     tr[tr.length - 1].lastChild.lastChild.onclick = function() {
        //         this.parentNode.parentNode.remove();
        //     };
        // };
        // // 删除按钮
        // del.onclick = function() {
        //         var inputChoose = document.getElementsByClassName('choose');
        //         var table = document.getElementsByTagName('table');
        //         for (let i = 0; i < inputChoose.length; i++) {
        //             if (inputChoose[i].checked == true) {
        //                 inputChoose[i].parentNode.parentNode.remove();
        //                 i--;
        //             }
        //         }
        //     }
        //     // 获取原来存在的a标签 绑定点击事件
        // var a = document.getElementsByTagName('a');
        // for (let i = 0; i < a.length; i++) {
        //     a[i].onclick = function() {
        //         this.parentNode.parentNode.remove();
        //     }
        // }
    </script>
</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/130648_8e692380_8254421.png "domtable.png") 
