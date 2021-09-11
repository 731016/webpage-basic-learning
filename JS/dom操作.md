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