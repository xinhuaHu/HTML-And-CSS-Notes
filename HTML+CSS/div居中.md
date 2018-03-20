## div 居中
1.  单行垂直居中
单容器内只有一行文字,设置实际高度height与所在行的行高line-height相等即可
```css
div{
	height: 50px;
	line-height: 50px;
	overflow: hidden;
}
```
overflow:hidden的设置是为了防止内容超出容器或者产生自动换行

