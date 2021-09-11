```html
<style>
    body {
        font-size: 20px;
    }
    
    div {
        float: left;
        margin-left: 5px;
        width: 200px;
        height: 200px;
        border: 1px solid darkgoldenrod;
    }
    
    .d1 {
        font-size: 2em;
    }
    
    .d2 {
        font-size: 2ex;
    }
    
    .d3 {
        font-size: 2rem;
    }
    
    .d4 {
        font-size: 80%;
        color: rgba(0, 0, 0, 0.2);
    }
</style>

<body>
    <div class="d1">
        文本字体em
    </div>
    <div class="d2">
        文本字体ex
    </div>
    <div class="d3">
        文本字体rem
    </div>
    <div class="d4">
        文本字体 %
    </div>
</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/105434_06dcea18_8254421.png "css单位.png")