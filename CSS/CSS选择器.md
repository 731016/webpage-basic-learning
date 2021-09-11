# 基础选择器
```html
<style>
    a {
        display: block;
    }
    
    div>a {
        font-size: 60px;
        color: red;
    }
    
    ul>li {
        color: sienna;
    }
    
    p:nth-of-type(2n) {
        font-family: "微软雅黑";
        color: slateblue;
        font-size: 20px;
    }
    
    ul li:nth-child(2) {
        color: red;
    }
    
    p[class] {
        border: 3px solid green;
    }
    
    p[class="c1"] {
        border: 4px solid blue;
    }
    
    p[class^="b"] {
        border: 2px solid yellowgreen;
    }
    
    p[class$="3"] {
        border: 2px solid grey;
    }
    
    p[class*="3"] {
        border: 9px solid darkmagenta;
    }
    
    .nine:hover {
        color: darkorange;
    }
</style>

<body>
    <div>
        <a href="">前 子</a> 张九龄《秋晚登楼望南江入始兴郡路》
        <p>
            <a href="">孙</a>
        </p>
        <a href="">后 子</a>

    </div>
    <ul>
        <li>马</li>
        <li>写马</li>
        <li>写马</li>
        <li>写马</li>
        <li>写马</li>
    </ul>
    <p class="c1">2、 〖写马〗 “白马谁家子，黄龙边塞儿。”…………李白《独不见》</p>
    <p class="c2">
        3、 〖写马〗 “驻马桥西，还系旧时芳树。”…………高观国《玲珑四犯·水外轻阴》

    </p>
    <p class="b3">
        4、 〖写马〗 “悠悠卷旆旌，饮马出长城。”…………李世民《饮马长城窟行》

    </p>
    <p class="c33">
        5、 〖竹子〗 “蜡炬风摇帘不下，竹影半墙如画。”…………项鸿祚《清平乐·池上纳凉》


    </p>

    <p>
        6、 〖写马〗 “傍枯林古道，长河饮马，此意悠悠。”…………张炎《八声甘州·记玉关踏雪事清游》

    </p>
    <p>
        7、 〖竹子〗 “苍苍竹林寺，杳杳钟声晚。”…………刘长卿《送灵澈上人》

    </p>
    <p>
        8、 〖写马〗 “细草软沙溪路、马蹄轻。”…………苏轼《南歌子·寓意》

    </p>
    <p class="nine">
        9、 〖竹子〗 “庭下如积水空明，水中藻、荇交横，盖竹柏影也。”…………苏轼《记承天寺夜游 / 记承天夜游》

    </p>

</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/105934_1a4350b1_8254421.png "css选择器.png")

# 属性选择器
```html
<style>
    table {
        margin: 100px auto;
        width: 500px;
        height: 500px;
        /* background-image: url(./images/爱心.png);
        background-repeat: no-repeat;
        background-position: center;
        background-attachment: fixed; */
        background: url(./images/爱心.png) no-repeat center scroll;
    }
    
    tr:hover {
        background-color: rgba(0, 0, 0, 0.5);
    }
    
    p:nth-of-type(1) {
        height: 30px;
        font-style: italic;
        font-weight: 700;
        font-size: 32px;
        line-height: 30px;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        /* 文本方向右对齐 */
        direction: rtl;
        /* 字体间距 */
        letter-spacing: 20px;
        /* 首行缩进 */
        text-indent: 10px;
        /* 文本阴影 */
        text-shadow: lightcoral 1px 1px 0.5px;
    }
    
    p:nth-of-type(2) {
        height: 30px;
        font-style: italic;
        font-weight: 700;
        font-size: 32px;
        line-height: 30px;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        /* 文本方向右对齐 */
        direction: rtl;
        /* 字体间距 */
        letter-spacing: 20px;
        /* text-indent: 10px; */
        text-shadow: lightcoral 1px 1px 0.5px;
    }
    
    ul>li {
        /* 简写属性 声明列表所有属性 */
        list-style: none;
        /* 列表项标志 */
        /* list-style-image: url(./images/爱心.png); */
        /* 列表项标志位置 */
        list-style-position: inside;
        /* 列表项标志类型 */
        list-style-type: georgian;
    }
</style>

<body>
    <p>去官方区划</p>
    <p>去官方区划</p>
    <div>
        <ul>
            <li>武汉市</li>
            <li>广州市</li>
            <li>杭州市</li>
        </ul>
    </div>
    <table border="" cellspacing="0" cellpadding="0">
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </table>

</body>
```
**效果展示**  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/112156_d3d6c917_8254421.png "3.png")