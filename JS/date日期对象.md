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