## javaScript

#### 基本语法

1. 数据类型

   | 基本数据类型    | 复杂数据类型 |
   | --------- | ------ |
   | number    | Array  |
   | string    | String |
   | boolean   | Number |
   | null      | Math   |
   | undefined | Date   |
   |           | JSON   |

   -   Array

       * 数组的创建

         ```javascript
         var arr = [];
         var arr = new Arra();
         ```

       * 数组API

         -   ```concat()```数组合并

             ```javascript
             var arr1 = [1,2,3];
             var arr2 = [4,5,6];
             arr1.concat(arr2);
             ```

         -   ```push()```数组末尾添加元素

             ```javascript
             arr.push(newElement1,....newElementn);
             ```

         -   ```unshift```数组开头添加元素

             ```javascrip
             arr.unshift(newElement1,....newElementn);
             ```

         -   ```splice```删除元素，并向数组添加新元素。删除或中间添加新的数据，对原数组直接进行操作

             ```javascript
             arr.splice(start, count, newData1, ..., new Datan)
             ```

         -   ```slice```从原数据中截取指定的数据，并产生新的数组。不会对原数组直接进行操作

             ```javascript
             var arr2 = arr.slice(start, end)
             ```

         -   ```pop```把数组的最后一个数据删除，并返回删除的数据

             ```javascript
             var a = arr.pop();
             ```

         -   ```shift```把数组的第1个数据删除，并返回删除的数据，所有数据都需要往前移1位

             ```javascript
             var a = arr.shift();
             ```

         -   `length`数组长度

             ```javascript
             var len = arr.length
             ```

         -   `join`把数组数据合并为一个字符串，如果不使用参数，默认使用,做数据与数据之间的分隔，如果写了参数使用参数的内容作为分隔符

             ```javascript
             var arr1 = [1, 2, 3];
             var a1 = arr.join()；
             var a2 = arr1.join('|');
             var a3 = arr1.join('');
             ```

   -   String

       -   字符串创建

           ```javascript
           var s = '';
           var s = String(a);
           var s = obj.toString();
           var s = new String('a')
           ```

       -   字符串API

           -   `charAt`返回在指定位置的字符

           -   `charCodeAt`返回在指定的位置的字符的 Unicode 编码。

           -   `concat`连接字符串。

           -   `indexOf`从左往右查询内容在字符串中第一次出现的位置，如果没有返回-1

           -   `lastIndexOf`从右往左查询内容在字符串中第一次出现的位置，如果没有返回-1

           -   `slice`从原字符串中截取指定的字符

               ```javascript
               /*
               stringObject.slice(start,end)语法
               */
               slice(0)            //从开始索引位置截取到字符串结束为止
               slice(4, 6)         //从开始索引位置截取到结束的索引位置
               slice(-3)           //从倒数开始索引位置截取到字符串结束为止
               slice(-8, -1)       //从倒数开始索引位置截取到倒数结束索引位置
               slice(6, 4)         //开始位置大于结束位置，返回0长度的字符串
               ```

           -   `substr`从开始索引位置截取到字符串结束为止

               ```javascript
               /*
               substr(start[, count])语法
               */
               substr(0);
               substr(0,4) //从开始索引位置截取到n个字符
               substr(-3)  //从倒数的n个字符截取到结束位置
               substr(-3, 4)//从倒数的n个字符截取m个字符
               ```

           -   `substring`类似于slice的使用

               ```
               区别：
               1. 如果开始位置大于结束位置，会自动换位，保证开始位置小于结束的位置
               2. 如果参数是负数，返回的是整个字符串内容
               ```

               ​

           -   `toUppercase`把英文字母转换为大写

           -   `toLowercase`把英文字母转换为小写

           -   `lenght`获取字符串长度

           -   `replace`字符替换

               ```javascript
               replace(old,new)//把old的内容替换为new的内容
               ```

   -   Number

       - Nunber创建

         ```javascript
         var myNum = Number(value);
         var myNum=Number(value);
         ```

       - 使用

         - `parseFlot`把数字转换为小数

         - `parseInt`把数字转换为整数

         - `toFixed`把数字转换为字符串，结果的小数点后有指定位数的数字。

           ```javascript
           1.234.toFixed(2)
           ```

   -   Math

       - 使用

         - `abs()`绝对值

           ```javascript
           var a = Math.abs(-1)
           ```

         - `floor()`向下取值

           ```javascript
           var a = Math.floor(val)
           ```

         - `celi()`向上取值

           ```javascript
           var a = Math.ceil(val)
           ```

         - `round()`四舍五入

           ```javascript
           var a = Math.round(val)
           ```

         - `random()`随机数

           ```javascript
           var a = Math.random(val)
           ```

   -   Date

       - 创建

         ```javascript
         var date = new Date()//获取当前主板时间
         var date = new Date('2017/7/1 12:00:00');
         var date = new Date('Tur 2018/4/14 9:25:10 GMT+0800');
         var date = new Date(2918, 4, 14, 9, 25, 19);
         ```

       - API

         ```javascript
         now.getFullYear()或now.setFullYear(2010)//年份
         now.getMonth()或now.setMonth(1)//月份   月份是从0开始计算
         now.getDate()或now.setDate(14)//当天日期
         now.getHours()或now.setHours()//小时
         now.getMinutes()或now.setMinutes(10)//分钟
         now.getSeconds()或now.setSeconds(10)//秒数
         now.getDay()或now.setDay(0)//一周的某一天
         getMilliseconds()//毫秒
         ```

       - 获取当前的毫秒

         ```javascript
         Date.now()
         +new Date()
         new Date().getgetMilliseconds()
         new Date().valueOf()
         ```

         ​

   -    JSON(以键值对出现的一种数据格式)

       -   创建

           ```javascript
           var json = {"name":"张三","age":16}
           ```

       -   获取

           ```javascript
           var name = json.name
           var name = json['name']
           ```

       -   赋值

           ```javascript
           json.name = '李四'
           json['name'] = '李四'
           ```

2. 流程控制

   -   分支

       -   if...else if...else

           ```javascript
           if(条件语句){
               执行语句
           } else if(条件语句){
               执行语句
           } else{
               执行语句
           }
           ```

       -   switch...case

           ```javascript
           switch(n){
           case 1:
               执行代码块 1
               break;
           case 2:
               执行代码块 2
               break;
           default:
               n 与 case 1 和 case 2 不同时执行的代码
           }
           ```

   -   循环

       -   for 确定循环次数

           ```javascript
           for(var i=0;i<length;i++){
               被执行的代码块;
           }
           ```

       -   while 不确定循环次数

           ```javascript
           while (条件){
               需要执行的代码
           }
           ```

       -   for...in 同常用于迭代JSON数据

           ```javascript
           var arr={'name':'张三','age':'25'};

           for(var key in arr){
               console.log(arr[key]);
           }
           ```

       -   do...while 确定要先执行一次

           ```javascript
           do{
               需要执行的代码
           }
           while (条件);
           ```

   -   关键字

       -   continue
       -   break

3. 变量

   -   形参


   -   实参

4. 函数

   -   创建

       ```javascript
       function(){};
       var fn = function(){};
       (function(){})();
       var fn = new function('alert();');
       ```

       ​

#### 定时器

1.  setInterval

    ```javascript
    var timer = setInterval(function(){}, 10)//创建定时器 间隔执行
    ```

2.  setTimeout

    ```javascript
    var timer = setTimeout(function(){}, 10)//创建定时器 只执行一次
    ```

3.  clearInterval

    ```javascript
    clearTimeout(timer)//清除定时器
    ```

4.  clearTimeout)

    ```javascript
    clearInterval(timer)//清除定时器
    ```



#### 样式相关

1.  获取元素

    -   document.getElementById() 获取id

    -   document.getElementsByTagName() 获取标签

    -   document.getElementsByClassName() 获取class

        IE8及以前浏览器不支持，需要自己使用getElementsByTagName('*')获取所有的标签元素，再通过循环检查className的值是否有我们查找的值，如果有把这个元素添加到数据，最后返回数组。

        ```javascript
        /**
         * 兼容IE8及以前版本使用getElementsByClassName
         * @param val               需要查找的类选择器名称
         * @returns {Array}
         */

        function getByClassName(val) {
            // 如果类选择器以.开始，需要把.去掉
            var className = val.indexOf('.') == 0 ? val.slice(1) : val;
            var arr = [];
            var all = $('*');

            for (i = 0, len = all.length; i < len; i++) {
                var tmp = all[i].split(' ');

                for (var j = 0, count = tmp.length; j < count; j++) {
                    if (tmp[j] == className) {
                        arr.push(all[i]);
                        break;
                    }
                }
            }
        }

        // 如果浏览器不支持getElementsByClassName，重写getElementsByClassName的实现行为
        document.getElementsByClassName = document.getElementsByClassName ? document.getElementsByClassName : getByClassName;   
        ```




2.  DOM节点操作

    ```javascript
    var li = document.createElement('li')  		//创建节点
    ul.appendChild(li)							//追加节点(最后)
    ul.insertBefore(li, otherLi)				//插入节点(指定节点或第一个节点，需要插入的节点)
    ul.removeChild(li)							//删除节点
    var textNode = document.createTextNode('1');//也可以通过innerHTML/innerText的形式往父节点里添加文本节点
    var arr = ul.children						//查找子节点
    var li = ul.firstChild						//获取父节点下的第一个子节点
    var li = ul.lastChild						//获取父节点下的最后一个子节点
    var li2 = li.nextElementSibling || li.nextSibling //获取子节点的下一个兄弟元素
    var li2 = li.previousElementSibling || li.previousSibling//获取上一个兄弟节点，类似于nextSibling
    var li = ul.children 						//获取父节点下的所有节点，如果IE5678包含注释内容。建议使用
    var ul = li.parentNode						//获取子节点的父节点(上一级标签)
    var newLi = li.cloneNode(true)				//true的时候会复制后代节点，而不写或false只会复制当前节点
    ```
    -   封装获取dom方法

        ```javascript
        /**
         * 对DOM的查找进行了封装，可以根据ID、类名或标签名进行查询
         * @param val               查询的内容
         * @returns {*}
         */
        function $(val) {
            if (val.charAt(0) === '#') {
                return document.getElementById(val.substr(1));
            } else if (val.charAt(0) === '.') {
                return document.getElementsByClassName(val.substr(1));
            } else {
                return document.getElementsByTagName(val);
            }
        }
        ```

        ​

        -   属性操作

        ```javascript
        li.setAttribute(key, value) //设置自定义属性：.setAttribute(名称, 值)
        li.getAttribute(key) //获取自定义属性：.getAttribute(名称)
        li.removeAttribute(key) //删除自定义属性：.removeAttribute(名称)
        ```

        例子

        ```html
        <!--点击百度下，打开百度的页面-->
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>Title</title>
            <style>
                p{
                    float: left;
                    cursor: pointer;
                }
            </style>
        </head>
        <body>
            <p index="http://www.baidu.com">百度一下</p>
        </body>
        </html>
        ```

        ​

        ```java
        var p = document.getElementsByTagName('p')[0];
        p.onclick = function(){
          	this.setAttribute('index', 'http://www.taobao.com');
          	console.log(this.getAttribute('index'));
        	this.removeAttribute('index');
        	var url = this.getAttribute('index');
        	window.location.href = url;
        }
        ```

#### 事件

```
	onclick
	onfocus
	onblur
	onscroll
	onmouseover
	onmouseout
	onmouseenter
	onmouseleave
	oninput
	onchange
	scrollTo(x, y)//模拟滚动条件滚动的事件，x和y参数都必须要提供。分别表示left和top的值
	click() //模拟鼠标的点击事件
```

#### 三大家族

1.  offset

    ```javascript
    offset与style的区别
        1.offset不允许修改，style可以
        2.style不能获取非行内样式设置的值，而offset可以获取
        3.offset获取的值不带单位，style获取的带有单位
    ```

    -   offsetWidth
    -   offsetHeight
    -   offsetTop
    -   offsetLeft

2.  scroll

    -   scrollWidth，width=width+溢出的宽度
    -   scrollHeight，width=width+溢出的宽度
    -   scrollTop，距离页面顶部的高度
    -   scrollLeft，距离页面左侧的宽度
    -   获取方式
        -   document.body.scrollTop或document.body.scrollLeft没有写DTD的情况才可以获取到具体的值，如果有DTD只能获取到0
        -   document.documentElement.scrollTop或document.documentElement.scrollLeft
        -   window.pageYOffset或window.pageXOffsetIE支持不好

3.  ​

#### 面向对象

#### 数据交互

#### 数据检验

