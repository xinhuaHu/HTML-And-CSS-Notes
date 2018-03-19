## 文本标签
### <strong> and <em> 都是强调
  *  strong 表示强调内容浏览器上用粗体表示  em 表示强调语气在浏览器上用斜体表示

```html
<p>
	<strong>这是strong</strong>
	<em>这是em</em>
</p>
```

### <i> and <b>
 * i 斜体显示 , b 粗体显示 , i 和 b 无语言 , 单纯为了加粗和斜体可以使用

```html
<p>
	<i>这是i</i>
	<b>这是b</b>
</p>
```
### small会比父元素中的小, 一般用于细则内容

```html
<p>
	这是p标签
	<small>这是small</small>
</p>
```

### cite 指明内容的引用或参考,表示书名,歌名,电影名等,斜体显示

```html
<p>
	<cite> 《论语》</cite>
</p>
```
### blockquote 和 q
 * q 短引用 默认添加引号 在行内
		blockquote 块级引用 在新行

```html
<p>
	子曰:<q>有朋自远方来,不亦说乎</q>
	子曰:<blockquote>温故而知新,可以为师矣</blockquote>
</p>
```
### sup 和 sub
* 定义上标和下标

```html
<p>
	10<sup>2</sup>
	H<sub>2</sub>O
</p>
```
### ins 和 del
* ins表示插入的内容，显示时通常会加上下划线.
* del表示删除的内容，显示时通常会加上删除线.

```html
<p>
	美女<ins>漂亮</ins>
	<del>丧心病狂</del>(干得漂亮)
</p>
```

### code 和 pre
* 内容包含代码示例或文件名 ，就可以使用code元素
* pre元素表示的是预格式化文本 , 可以包涵code元素表示代码

```html
<pre>
    <code>
        function fun(){
            alert("hello");
    }
    </code>
</pre>
```

### 列表

* ul 无序列表
```html
    <ul>
        <li>21</li>
        <li>23</li>
        <li>13</li>
    </ul>
```

* ol 有序列表
```html
    <ol>
        <li>21</li>
        <li>23</li>
        <li>13</li>
    </ol>
```

* dl 自定义列表 ,以dt作为自定义列表项开始, dd为自定义列表项的定义开始
```html
    <dl>
        <dt>1</dt>
        <dd>first number</dd>
        <dt>2</dt>
        <dd>second number</dd>
        <dt>3</dt>
        <dd>three number</dd>
    </dl>
```

* 列表嵌套
```html
<ol>
	<li>处理图像</li>
		<ol  type="a">
			<li>312</li>
			<li>312</li>
			<li>312</li>
		</ol>
	<li>处理表格</li>
		<ol  type="A">
			<li>312</li>
			<li>312</li>
			<li>312</li>
			<ol  type="I">
				<li>312</li>
				<li>312</li>
				<li>312</li>
			</ol>
		</ol>
	<li>创建项目符号列表或编号列表</li>
</ol>
```
## HTML表格

* tr:行标签
* td:单元格标签
* th:表头,字体会加粗
```html
<table boder="1px">
    <tr>
        <th>mane</th>
        <th>munber</th>
        <th>passwd</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>guest</td>
        <td>luogou</td>
    </tr>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    <tr><td>3</td>
        <td>2</td>
        <td>1</td>
    </tr>
</table>
```

* colspan:合并行单元格
* rowspan:合并列单元格
```html
<table border="1px">
    <tr>
        <td rowspan="2">123</td>
        <td>123</td>
        <td>123</td>
        <td>123</td>
    </tr>
    <tr>
        <td colspan="2">123</td>
        <td>123</td>
    </tr>
    <tr>
        <td>123</td>
        <td>123</td>
        <td>123</td>
        <td>123</td>
    </tr>
</table>

```
