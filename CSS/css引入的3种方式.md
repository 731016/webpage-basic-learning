```html
<!-- 内部样式表 -->
    <style>
        .p1 {
            width: 150px;
            height: 20px;
            color: burlywood;
            font-weight: 700;
            margin: 20px auto;
        }
        
        .d1 {
            width: 100%;
            height: 200px;
            background: linear-gradient(to right, red, yellow);
        }
        
        .d2 {
            width: 100%;
            height: 200px;
            background: linear-gradient(to bottom right, red, yellow);
        }
    </style>
</head>
<link rel="stylesheet" href="./css/hello.css">

<body>
    <!-- 内嵌式 -->
    <p style="width: 150px;height: 20px;color: blueviolet;font-weight: 700;font-size: 16px;margin: 10px auto;">今天很热！！！</p>
    <p class="p1">css基础</p>
    <a href="#">点击触发 Hello World</a>
    <div class="d1"></div>
    <div class="d2"></div>
</body>
<script src="./js/hello.js"></script>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/111401_cca103b6_8254421.png "css引入.png")
