# Web开发零基础

学习路线：前端 HTML、CSS、JavaScript（JS） ——> Ajax、Axios ——> Vue、Element ——> 前端工程化（Vue脚架）——> Maven ——> Springboot基础 ——> Springboot基础，SpringMVC基础 ——> Mysql ——> JDBC、Mybatis ——> Web案例（基于Springboot整合SSM（前三项））——> 会话跟踪技术（Cookie、Session、令牌技术JWT）——> Filter Interceptor（令牌的统一拦截校验）——> AOP ——> Springboot原理



## 一、Web开发

Web称为万维网（www）全称 world wide web 能够通过浏览器访问的网站

Web开发模式：

![image-20240213203633439](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240213203633439.png)

使用的技术展示：

![image-20240213203852457](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240213203852457.png)

## 二、前端开发

### 插件介绍

下载管理插件的位置，不使用该插件可以右键选择禁用或卸载

![image-20240526114649969](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240526114649969.png)

(1) Live Server 实时刷新插件，写代码时实时预览效果 ，不需要手动刷新

(2) indent-rainbow 彩色缩进插件，缩进的位置有彩色

(3)  Bracket Pair Colorizer 区分不同括号的颜色

(4) 格式化代码，保存会自动格式会代码（已配置）

(5) code-transform 翻译单词（鼠标悬浮）

(6) 同步修改标签功能（已配置）

(7) Prettier - Code formatter 格式化插件

(8) JavaScript (ES6) code snippets

(9) CSS Peek 定位引入的地方

(10) JavaScript (ES6) code snippets 快捷插入一段代码

(11) Vetur    Vue的相关插件

(12) Simple React Snippets    React相关的插件

(13) Angular Snippets (Version 16)  && Angular Language Service && Angular Language Service    Angular相关的插件

------

Web标准

前端的三个组成部分：HTML（负责网页结构）、CSS（负责网页的表现，外观位置样式等）、JavaScript：负责网页的行为（交互效果，可动）

HTML：HyperText Markup Language 超文本标记语言

◆超文本:超越了文本的限制，比普通文本更强大。除了文字信息，还可以定义图片、音频、视频等内容。
◆标记语言:由标签构成的语言。
➢HTML标签都是预定义好的。例如:使用<a>展示超链接,使用<img>展示图片, <video>展示视频。
➢HTML代码 直接在浏览器中运行, HTML标签由浏览器解析。



CSS (Cascading Style Sheet) :层叠样式表，用于控制页面的样式(表现)。



HTML中的标签不区分大小写，src可以使用双引号或者单引号

```HTml
<html>
		<head>
				<title>yhw HTML 快速入门</title>
		</head>
		<body>
				<h1> Hello HTML</h1>
				<img src = "1.png"/>  自闭和用一个斜杠或者类似于前面<>
		</body>
</html>
```

颜色的表示方法

![image-20240214162300167](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240214162300167.png)

超链接：

![image-20240214165035909](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240214165035909.png) 



在HTML中无论输入多少个空格，只会显示一一个。可以使 用空格占位符:&nbsp



盒子模型

![image-20240215100354519](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240215100354519.png)

### 1.标题排版1

```HTML
<!-- 添加注释 ctrl + / -->
<!-- ！+ 回车  -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 字符集为UTF—8 -->
    <meta charset="UTF-8">
    <!-- 设置浏览器的兼容性 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>新浪微博</title>
</head>
<body>
    <!-- 
    img标签：
    src：资源路径
    width：宽度  （像素px / 百分比% 相对于父元素）
    height：高度
     -->
     <!-- 相对路径写法：  绝对路径需要加盘符或者用网络路径 -->
     <!-- ./表示当前目录可以省略 ../表示上一级目录 -->
     <!-- 只设置宽度或高度等比例变形 -->
     <!-- <img src="./img/logo.png" width="300px"> -->
     <!-- <img src="./img/logo.png" width="80%"> -->
     <img src="./img/logo.png"> 新浪政务 > 正文
     <h1>
        焦点访谈：中国底气新思想夯实大国粮仓
     </h1>
     <hr>
     2024年2月14日 15:30 央视网
    <hr> 
</body>
</html>
```

### 2.标题排版2

```HTML
<!-- 添加注释 ctrl + / -->
<!-- ！+ 回车  -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 字符集为UTF—8 -->
    <meta charset="UTF-8">
    <!-- 设置浏览器的兼容性 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- 方式2：内嵌样式 -->
    <style>
        h1{
            /* 关键词表示法： */
            /* color:brown; */
            
            /* 三原色表示法： */
            /* color:rgb(255,12,255) */

            /* 十六进制表示法：相同两位可以缩写为一位等价于 f00 */ 
            /* color:#ff0000 */

        }
    </style>
    <!-- 方式3：外联样式，将样式定义在其他文件夹里面 -->
    <link rel="stylesheet" href="css/new.css">
    <title>新浪微博</title>
</head>
<body>
    <div id = "center">
        <!-- <a>超链接，href指定资源访问的url，target指定在何处打开资源链接，_self 默认值当前页面打开，_blank空白页面打开 -->
        <img src="./img/logo.png"> <a href="http://gov.sina.com.cn/" target="_self">新浪政务</a>  > 正文
        <!-- 方式1：行内样式 -->
        <!-- <h1 style="color: chocolate;">
            焦点访谈：中国底气新思想夯实大国粮仓
        </h1> -->
        <h1>
            焦点访谈：中国底气新思想夯实大国粮仓
        </h1>
        <hr>

        <!-- span将一行的内容分块，还是一行无其他意义 -->
        <span class="cls">2024年2月14日 15:30</span>
        <span id = "time"> <a href="https://news.cctv.com/2023/03/02/ARTIUCKFf9kE9eXgYE46ugx3230302.shtml" target="_blank">央视网</a> </span>
        <hr>
        <!-- 正文 -->
        <!-- 视频 -->
        <!-- controls 是显示视频的播放控件 -->
        <video src="video/1.mp4" controls width="950px"></video>
        <!-- 音频 -->
        <!-- <audio src="audio/1.mp3" controls></audio> -->

        <p>
            <!-- b加粗 -->
            <!-- strong强调 -->
            <b>央视网消息</b>
            <strong>(焦点访谈) :</strong>党的十八大以来，以习近平同志为核心的党中央始终把解决粮食安全问题作为治国理政的头等大事，重农抓粮一-系
            列政策举措有力有效，我国粮食产量站稳1.3万亿斤台阶，实现谷物基本自给、口粮绝对安全。我们把饭碗牢牢端在自己手中，为保障经济社
            会发展提供了坚实支撑，为应对各种风险挑战赢得了主动。连续八年1.3万亿斤，这个沉甸甸的数据是如何取得的呢?
        </p>
        <img src="img/2.png">
        <p>
            人勒春来早，春耕农事忙。立春之后，由南到北，我国春耕春管工作陆续展开，春天的田野处处生机盎然。
        </p>
        <!-- 在HTML中无论输入多少个空格，只会显示一一个。可以使 用空格占位符: &nbsp; -->
        <p id = "plast">
            责任编辑：杨皓文
        </p>
    </div>
</body>
</html>
```

### 3.CSS设置            

```css
/* 优先级ID大于类大于元素 */
/* 元素选择器 */
h1{
    color:#4D4F53;
}
/* 类选择器 */
.cls{
    /* 字体大小的设置 */
    font-size:13px;
    color: #968D92;
}
/* id选择器 */
#time{
    color: burlywood;
}
a{
    /* 取出下划线 */
    text-decoration: none;
    color: black;
}
p{
    /* 设置首行缩进 */
    text-indent: 30px;
    /* 设置行高 */
    line-height: 40px;
}
#plast{
    /* 设置靠右对齐 */
    text-align: right;
}

#center{
    /* 让整个居中展示 */
    width: 65%;
    /* margin只有个两个值的话分别表示上下边距和右左边距，三个值分别表示上、右左、下 */
    /* margin: 0% 17.5% 0% 17.5%; */
    /* 等价于 auto浏览器会自动计算*/
    margin: 0 auto;
}
```

### 4.盒子模型

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>盒子模型</title>
    <style>
        /* 盒子不包含外边距margin */
        div{
            /* 设置盒子的大小 */

            width: 200px;
            height: 200px;
            /* 不设置下面这个属性则上面指的是盒子的内容区域的宽高 */
            /* 设置了则指的是border的宽高 */
            box-sizing: border-box;
            background-color: aquamarine;

            /* 内边距 上 右 下 左 */
            /* 都一样可以简写为一个20px */
            padding: 20px 20px 20px 20px;
            /* 边框，宽度 线条类型 颜色 */
            border: 10px solid red;
            /* 外边距 上 右 下 左 */
            margin: 30px 30px 30px 30px;
        }
    </style>
</head>
<body>
    <div>
        A A A A A A A A A A
    </div>
</body>
</html>
```

### 5.表单项标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>表单项标签</title>
</head>
<body>
    <form action="" method="post">
        <!-- <br>是换行 -->
        姓名：<input type="text" name="name"><br><br>
        密码：<input type="password" password="password"><br><br>
        <!-- radio是单选框 value是对应点击后提交的值 label是将文字的点击效果绑定到选项上 -->
        性别：<label><input type="radio" name="gender" value="1"> 男</label>
              <label><input type="radio" name="gender" value="1"> 女</label><br><br>
        爱好：<label><input type="checkbox" name="hobby" value="java"> java </label>
             <label><input type="checkbox" name="hobby" value="game"> game </label>
             <label><input type="checkbox" name="hobby" value="sing"> sing </label>
             <br><br>
        图像：<input type="file" name="image"><br><br>
        生日：<input type="date" name = birthday> <br><br>
        时间：<input type="time" name="time"> <br><br>
        日期时间：<input type="datetime-local" name="datetime"> <br><br>
        邮箱：<input type="email" name="email"> <br><br>
        年龄：<input type="number" name="age"> <br><br>
        <!-- 下拉列表 -->
        学历：<select name="degree">
            <option value="">--------- 请选择 ---------</option>
            <option value="1">大专</option>
            <option value="2">本科</option>
            <option value="3">硕士</option>
            <option value="4">博士</option>
        </select><br><br>
        <!-- textarea定义文本域 cols一行可以输入多少个字符，rows可以输入多少行 -->
        描述：<textarea name="description" cols="30" rows="10"></textarea><br><br>
        <!-- 隐藏域 -->
        <input type="hidden" name="id" value="1">

        <!-- 表单常见的按钮 -->
        <input type="button" value="按钮">
        <input type="reset" value="重置">
        <input type="submit" value="提交">
        <br>
    </form>
</body>
</html>
```

### 6.表格

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>表格</title>
</head>
<body>
    <h1>手机品牌信息表</h1>
    <!-- border设置有边框 cellspacing设置两个单元格之间的距离为0 -->
    <table border="1px" cellspacing="0" width="600px">
        <!-- 每一个tr对应一行 t row -->
        <tr>
            <!-- 表头单元格用th t head -->
            <th>序号</th>
            <th>品牌logo</th>
            <th>品牌名称</th>
            <th>企业名称</th>
        </tr>
        <tr>
            <!-- td 定义普通单元格 -->
            <td>1</td>
            <td><img src="img/huawei.jpg" width="100px"></td>
            <td>华为</td>
            <td>华为技术有限公司</td>
        </tr>
        <tr>
            <td>2</td>
            <td><img src="img/alibaba.jpg" width="100px"></td>
            <td>阿里</td>
            <td>阿里巴巴有限公司</td>
        </tr>
    </table>
</body>
</html>
```



### 7.JavaScript 

JavaScript是一门跨平台、面向对象的脚本语言。只需要被解释不需要被编译。

JS的基础语法：

Ctrl + 斜杆 单行注释 + Shift 多行注释

![image-20240217225014505](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240217225014505.png)

JSON概念: JavaScript Object Notation, JavaScript对象标记法。
JSON是通过JavaScript对象标记法书写的文本。

由于其语法简单，层次结构鲜明，现多用于作为数据载体,在网络中进行数据传输。

JSON的基础语法

![image-20240219161926825](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240219161926825.png)

BOM：

概念: Browser Object Model浏览器对象模型，允许JavaScript与 浏览器对话，JavaScript 将浏览器的各个组成部分封装为对象。

主要为一下5个对象：

![image-20240219170529378](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240219170529378.png)



window对象：

![image-20240219170737957](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240219170737957.png)



DOM：概念: Document Object Model，文档对象模型。
将标记语言的各个组成部分封装为对应的对象:

![image-20240219174804594](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240219174804594.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS</title>
    <!-- alert提醒窗口 -->
    <!-- 内部脚本，可以定义在html内的任意位置 -->
    <!-- <script>
        完整写法window.alert("")
        alert("hello 杨皓文")
    </script> -->
    <!-- 外部脚本 -->
    <script src="js/demo.js"></script>
</head>
<body>
    <!-- <script>
        alert("hello 杨皓文")
    </script> -->
    <img id="h1" src="img/off.gif"> <br><br>
    <div class="cls">传智教育</div> <br>
    <div class="cls">黑马程序员</div> <br>

    <input type="checkbox" name="hobby"> 电影
    <input type="checkbox" name="hobby"> 旅游
    <input type="checkbox" name="hobby"> 游戏
</body>
<!-- <script>
    // 方式一：弹出警告框
    window.alert("杨皓文你好")

    // 方式二：写入html页面
    document.write("yhw你好")

    // 方式三：控制台输出
    console.log("hello yhw")
</script>
<script>
    // var用来定义变量
    // 特点1：作用域比较大，全局变量
    // 特点2：可以重复定义
    var a = 10;
    a = "张三"
    alert(a)
    {
        var x = 1;
        var x = "yhw"
        alert(x)
    }
    // let局部变量 不能重复定义
    {
        let y = 1
        alert(y)
    }
    alert(x)
    // const 声明常量不能改变
    const pi = 3.14
</script> -->
<!-- 变量 -->
<!-- <script>
    var a
    alert(typeof a)         //undefined
    a = 1
    alert(typeof a)         //number
    a = 3.14
    alert(typeof a)         //number
    a = 'yhw'
    alert(typeof a)         //string
    a = "yhw"
    alert(typeof a)         //string
    a = null
    alert(typeof a)         //object 早期bug导致
    a = true
    alert(typeof a)         //boolean
    a = false
    alert(typeof a)         //boolean
</script> -->
<!-- 基础 -->
<!-- <script>
    var age1 = 20
    var age2 = "20"
    var age3 = 20
    // 先判断类型是否一样，不一样将类型转化为一样再进行比较
    alert(age1 == age2)         //true
    // 全等于只有类型和值都一样才是true
    alert(age1 === age2)        //false
    alert(age1 === age3)        //true

    // 类型转换
    // 转化为数字
    alert(parseInt("12"))               //12
    alert(parseInt("12A45"))            //12
    alert(parseInt("A12"))              //NaN 不是一个数字not a number

    // 转换为boolean
    // 0和NaN，空字符串，null和undefined转化为boolean为false其余的都为true
</script> -->
<!-- 函数 -->
<!-- <script>
    // 定义函数function 方法1
    function add(a,b){
        return a+b;
    }
    // 方法2
    var add=function(a,b){
        return a+b;
    }
    // JS中函数调用可以传递任意个参数，多余的只是未被接收
    var sum = add(10,20)
    alert("a+b的和为"+sum)
</script> -->
<!-- 数组 -->
<!-- <script>
    // 数组的定义的两种方式
    var arr = new Array(1,2,3,4)
    var arr1 = [1,2,3,4]
    // for(var i = 0;i<4;i++){
    //     console.log(arr[i]);
    // }

    // 数组的长度可变，类型可变
    arr1[10] = "yhw"
    for(let i = 0;i < arr1.length;i ++){
        console.log(arr1[i])
    }

    console.log(arr1);

    console.log("forEach遍历");
    // forEach遍历有值的元素或者用function(e)
    // lambda表达式
    arr1.forEach(element => {
        console.log(element);
    });

    // 数组末尾添加元素
    arr1.push(5,6,7)
    console.log(arr1);

    // 从哪个元素开始删，删几个元素
    arr1.splice(1,2)

</script> -->
<!-- 字符串的定义 -->
<!-- <script>
    var str = new String("yhwhhh");
    var str2 = "  yhw  ";
    console.log(str.length);
    console.log(str+"\n"+str2);
    
    str2.charAt(1)
    // 检索位置
    str2.indexOf("yhw")
    // 去除字符串前后的空格 类似于py中的strip
    var s = str2.trim()
    console.log(s);
    // 截取子字符串
    console.log(str2)
    var s1 = str2.substring(0,4)
    console.log(s1)
</script> -->
<!-- 对象 -->
<!-- <script>
    var user = {
        name: "Tom",
        age: 20,
        eat:function(){
            alert("吃饭！");
        },
        // 可以省略为：
        eat2(){
            alert("吃饭");
        }
    }
    console.log(user.name);
    user.eat2()

    // JSON格式,json是一个文本
    var jsonstr = '{"name":"yhw","age":20,"boy":true,"addr":[1,2,3,4]}';
    
    // Json字符串转化为js对象
    var obj = JSON.parse(jsonstr);
    alert(obj.name)
    // js对象转换为JSON字符串
    alert(JSON.stringify(obj))
</script> -->
<!-- <script>
    // 获取window对象window可以省略
    window.alert("杨皓文在哪");
    
    // 方法 点击确认返回true，取消返回false
    var flag = confirm("你确认要删除记录吗？")
    // 定时器，周期性的执行某一个函数 单位是毫秒
    var i= 0;
    var i= 0;
    setInterval(function(){
        i++;
        console.log("定时器执行了"+i+"次");
    },1000)
    // 设定时间，多少时间后执行一次
    setTimeout(function(){
        alert("setTimeout正在执行")
    },1000)

    // location对象
    // 获取当前地址
    alert(location.href)
    // 修改当前地址
    location.href = "https://www.itcast.cn"
</script> -->
<!-- DOM获取和调用HTML的元素对象 -->
<!-- <script>
    // 根据id获取
    var img = document.getElementById("h1");
    alert(img);
    // 根据标签获取
    var divs = document.getElementsByTagName("div");
    for (let i = 0; i < divs.length; i++) {
        alert(divs[i]);
    }
    // 根据name属性获取
    var ins = document.getElementsByName("hobby");
    for (let i = 0; i < ins.length; i++) {
        alert(ins[i])
    }
    // 根据class属性获取
    var divs2 = document.getElementsByClassName("cls");
    for (let i = 0; i < divs.length; i++) {
        alert(divs[i])
    }

    // 查询参考手册，修改元素
    var div3 = divs2[0];
    // innerHTML设置或返回元素的内容
    div3.innerHTML = "传智教育666"
</script> -->
<!-- DOM案例 -->
<script>
    // 1.点亮灯泡 src：属性值
    var img = document.getElementById("h1");
    img.src = "img/on.gif";
    // 2.div标签后的内容都加上very good
    var divs = document.getElementsByTagName("div");
    for (let i = 0; i < divs.length; i++) {
        const element = divs[i];
        element.innerHTML += "<font color = 'red'>very good</font>"
    }
    // 3.使所有复选框呈现被选中状态
    var ins = document.getElementsByName("hobby");
    for (let i = 0; i < ins.length; i++) {
        const element = ins[i];
        // 使复选框呈现被选中的状态
        element.checked = true;        
    }
</script>
</html>
<!-- <script>
    alert("hello 杨皓文")
</script> -->

```



### 8.事件绑定

![image-20240220114556582](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240220114556582.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>事件绑定 - 案例</title>
</head>
<body>
    <img src="img/off.gif" id = "light"> <br>

    <input type="button" id = "bt1" value = "点亮" onclick="on()">
    <input type="button" id = "bt2" value = "熄灭">
    <br><br>
    <!-- onfocus 聚焦，onblur 离焦 -->
    <input type="text" id = "name" value = "ITCAST" onfocus="lower()" onblur="upper()"> <br><br>
    <input type="checkbox" name = "hobby"> 电影
    <input type="checkbox" name = "hobby"> 旅游
    <input type="checkbox" name = "hobby"> 游戏
    <br>
    <input type="button" value = "全选" onclick="checkAll()">
    <input type="button" value = "反选" onclick="reverse()">
</body>
<script>
    // 第1种事件绑定
    function on(){
        document.getElementById("light").src = "img/on.gif";
        console.log("点亮灯泡！");
    }
    // 第2中绑定的方法
    document.getElementById("bt2").onclick = function(){
        document.getElementById("light").src = "img/off.gif";
        console.log("熄灭灯泡！");
    }

    function lower(){
        var str = document.getElementById("name");
        str.value = str.value.toLowerCase();
    }
    function upper(){
        var str = document.getElementById("name");
        str.value = str.value.toUpperCase();
    }

    function checkAll(){
        var hobbys = document.getElementsByName("hobby");
        for (let i = 0; i < hobbys.length; i++) {
            const element = hobbys[i];
            element.checked = true;
        }
    }
    function reverse(){
        var hobbys = document.getElementsByName("hobby");
        for (let i = 0; i < hobbys.length; i++) {
            const element = hobbys[i];
            element.checked = false;
        }
    }
</script>
</html>
```

### 9.Vue

Vue是一套前端框架,免除原生JavaScript中的DOM操作，简化书写。
基于MVVM(Model-View-ViewModel)思想，实现数据的双向绑定，将编程的关注点放在数据上。

Model是数据模型，View是视图只负责视图的展示，ViewModel是两者通信的桥梁，可以完成两者的数据绑定

常用指令：

![image-20240220233942380](C:\Users\杨皓文\AppData\Roaming\Typora\typora-user-images\image-20240220233942380.png)