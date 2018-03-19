## HTML表格

* tr:行标签
* td:单元格标签
* th:表头,字体会加粗
```html
<table border="1px">
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

## 列表

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