```html
<body>
    <a href="http://www.baidu.com">点击跳转</a>
    <input type="button" value="打开窗口">
    <input type="button" value="关闭窗口">
    <input type="button" value="后退窗口">
    <script>
        // 窗口历史记录对象
        console.log(window.history);
        //当前窗口的url
        console.log(window.location);
        // window.location = "http://www.baidu.com";
        var newWin;
        document.getElementsByTagName('input')[0].onclick = function() {
            newWin = window.open('http://www.baidu.com', 'baidu', 'width=500,height=600');
        };
        document.getElementsByTagName('input')[1].onclick = function() {
            newWin.close();
        };
        document.getElementsByTagName('input')[2].onclick = function() {
            // history.back();
            //后退一个页面-1 1前进一个页面
            history.go(-1);
        };
    </script>
</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/114943_66116049_8254421.png "location.png")