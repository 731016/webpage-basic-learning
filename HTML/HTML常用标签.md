# 常用标签
```html
    <!--标题h1~h6-->
    <h1>hello world</h1>

    <!-- ctrl+? 注释-->

    <p>p标签</p>

    <strong>语义化加粗</strong>
    <b>加粗</b>

    <!-- 换行 -->
    <br>

    <i>斜体</i>
    <em>语义化斜体</em>

    <b><i>加粗斜体</i></b>

    <!-- 换行 -->
    <br> 空&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;格
```
<strong>展示效果</strong>  
![常用标签](https://images.gitee.com/uploads/images/2021/0911/100704_56cd486f_8254421.png "1.png")

# 超链接
```html
<a href="https://blog.csdn.net/qq_41666142?spm=1000.2115.3001.5343" target="">超链接</a>
    <a href="#m1">点击跳转m1</a>
    <a href="#m2">点击跳转m2</a>
    <p>近期，中澳关系迅速恶化，贸易行业受到了严重冲击，尤其是煤炭行业。 迄今为止，中国和澳大利亚&trade;将近6个月没有煤炭往来了。 &reg;澳大利亚&copy;丢了最大的煤炭市场而不自知，转投印度和越南市场，反倒使自己的煤炭行业面临滞销的局面。 而作为&ensp;盟&emsp;友，美国却趁机占领了中国的煤炭市场，&quot;彻底&quot;抢了澳大利亚的饭&amp;碗。
    </p>
    &lt; &gt;
    <a name="m1">锚点name</a>
    <a href="#">跳转到本页面</a>
    <p id="m2">锚点id</p>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/101142_8dc871ae_8254421.png "2.png")

# 列表标签
```html
<!--无序列表-->
    <ul>
        <li type="circle">shf1</li>
        <li type="disc">shf1</li>
        <li type="square">qarff</li>
        <li style="list-style: none;">afsdf</li>
    </ul>

<!--有序列表-->
    <ol type="A">
        <li>dwf</li>
        <li>dwf</li>
    </ol>
    <ol type="a">
        <li>dwf</li>
        <li>das</li>
    </ol>
    <ol type="I">
        <li>dwf</li>
        <li>fs</li>
    </ol>
    <ol type="i">
        <li>dwf</li>
        <li>gdfh</li>
    </ol>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/101433_ebaf2083_8254421.png "3.png")

# 表格标签
```html
<table align="center" border="" cellspacing="0" cellpadding="0" style="box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, .2);">
        <thead>
            <tr>
                <th>学生成绩</th>
                <th colspan="2"></th>

            </tr>
        </thead>
        <tbody>
            <tr>
                <td rowspan="2"></td>
                <td>语文</td>
                <td>98</td>
            </tr>
            <tr>
                <td>数学</td>
                <td>78</td>
            </tr>
        </tbody>
    </table>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/101603_dce0c109_8254421.png "4.png")

```html
<table border="" cellspacing="0" cellpadding="0" align="center" style="width: 600px;height: 200px;background-color: #a2c0e2;;text-align: center;box-shadow: 10px 8px 5px #017CFC;">
        <thead style="background: orange;">
            <tr>
                <th>姓名</th>
                <th>年龄</th>
                <th>工号</th>
                <th>电话号码</th>
                <th>工资</th>
                <th>工资时长</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>擅自</td>
                <td>34</td>
                <td>235363</td>
                <td>123254657567</td>
                <td>￥7855</td>
                <td>3年</td>
            </tr>
            <tr>
                <td>服务而如果</td>
                <td>34</td>
                <td>235363</td>
                <td>123254657567</td>
                <td>￥7855</td>
                <td>3年</td>
            </tr>
            <tr>
                <td>二分</td>
                <td>34</td>
                <td>235363</td>
                <td>123254657567</td>
                <td>￥7855</td>
                <td>3年</td>
            </tr>
            <tr>
                <td valign="top">问题个人</td>
                <td>34</td>
                <td>235363</td>
                <td>123254657567</td>
                <td>￥7855</td>
                <td>3年</td>
            </tr>
        </tbody>

    </table>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/101710_e864812f_8254421.png "5.png")

# 表格的单元格合并
```html
<table border="" align="center" cellspacing="0" cellpadding="0" style="width: 600px;height: 400px;">
        <tr bgcolor="red">
            <td></td>
            <td rowspan="2"></td>
            <td colspan="2"></td>
            <!-- <td></td> -->
            <td rowspan="3"></td>
        </tr>
        <tr>
            <td></td>
            <!-- <td></td> -->
            <td></td>
            <td rowspan="3"></td>
            <!-- <td></td> -->
        </tr>
        <tr>
            <td colspan="3"></td>
            <!-- <td></td>
            <td></td> -->
            <!-- <td></td> -->
            <!-- <td></td> -->
        </tr>
        <tr>
            <td colspan="2"></td>
            <!-- <td></td> -->
            <td></td>
            <!-- <td></td> -->
            <td></td>
        </tr>
    </table>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/101823_f032fe85_8254421.png "单元格.png")

# 表单标签
```html
<!-- <form action="./llk.html" method="GET">
        <input type="text">
        <input type="submit" value="提交">
        <input type="reset" value="重置">
    </form> -->
    <form id="post-submit" action="./llk.html" method="POST" style="margin: auto;width: 400px;">
        <input id="username" name="username" type="text" placeholder="请输入用户名" style="height: 50px;">
        <br>
        <input type="number" placeholder="请输入数字" style="height: 50px;">
        <br>
        <input type="date" style="height: 50px;">
        <br>
        <input type="time" style="height: 50px;">
        <br>
        <input type="datetime-local" style="height: 50px;">
        <br>
        <input type="color">
        <br>
        <input type="radio" name="gender" id="" value="1">男
        <input type="radio" name="gender" id="" value="0">女
        <br>
        <input type="checkbox" name="" id="" checked="checked">123
        <input type="checkbox" name="" id="">sf
        <input type="checkbox" name="" id="">fse
        <br>
        <input style="height: 50px;" id="password" name="pwd" type="password" maxlength="12" placeholder="请输入密码" style="margin-bottom: 20px;">
        <br>

        <input type="submit" value="提交" style="color: #fff;background-color: #1b86e0;">
        <input type="reset" value="重置" style="margin: 0 100px 0 100px;color: #fff;background-color: #1b86e0;">
        <input type="button" value="登录" style="color: #fff;background-color: #1b86e0;">
    </form>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/101950_b737c47c_8254421.png "b1.png")

# 下拉选择框
```html
<form action="#" method="GET">
        <!--进度条-->
        <input type="range" name="" id="" style="width: 300px;"><br> 你所在的城市？
        <select name="" id="" style="height: 50px;">    
            <option value="">请选择城市</option>
            <option value="杭州">杭州</option>
            <option value="成都">成都</option>
            <option value="上海">上海</option>
        </select>
        <br> 用户留言：<br>
        <textarea name="" id="" cols="30" rows="10" style="resize: none;width: 400px;height: 300px;font-family: Consolas;">

        </textarea><br>
        <input type="file" name="" id="">
        <input type="button" value="按钮">
        <button disabled>按钮</button>

    </form>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/102201_52f5c274_8254421.png "b2.png")

```html
<form action="#" method="POST">
        <fieldset style="width: 800px;">
            <legend>个人资料</legend>
            <label for="search">搜索框</label>
            <input type="search" name="search" id="search"><br>
            <!-- 隐藏域 -->
            <input type="hidden" name="id" value="admin">
            <input type="submit" value="提交"><br>
        </fieldset>
    </form>
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/102329_97c15182_8254421.png "b3.png")

# 内嵌网页
```html
<iframe src="./register.html" frameborder="0" style="width: 1200px;">
    </iframe>
    <iframe id="inlineFrameExample" title="Inline Frame Example" width="300" height="200" src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&layer=mapnik">
```
<strong>展示效果</strong>  
![输入图片说明](https://images.gitee.com/uploads/images/2021/0911/102506_9cffb845_8254421.png "iframe.png")