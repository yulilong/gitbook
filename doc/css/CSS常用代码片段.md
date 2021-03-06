[TOC]

### 1. 高度自适应屏幕高度

例子： 网站底部的版权条，当内容不足一屏的时候显示在屏幕的底部，在内容超过一屏的时候显示在所有内容的底部。

使用flex布局：

```html
<style>
    .container { display: flex; min-height: 100vh;
        flex-direction: column;
    }
    header { background: #cecece; min-height: 100px;
    }
    content { background: #bbbbbb;
        flex: 1; /* 1 代表盡可能最大，會自動填滿除了 header footer 以外的空間 */
    }
    footer { background: #333333; min-height: 100px; }
</style>
<div class="container">
  <header></header>
  <content></content>
  <footer></footer>
</div>
```

这样`<footer>`就会在底部了。

参考资料：https://blog.csdn.net/u014374031/article/details/69258208



### 2. a标签去掉下划线



```html
<style type="text/css">
a:link,a:visited{
 text-decoration:none;  /*超链接无下划线*/
}
a:hover{
 text-decoration:underline;  /*鼠标放上去有下划线*/
}
</style>

<a href="#">超链接</a>
```



### 3. input输入框输入时去掉默认蓝边

```less
input {
    &:focus {
        outline: none;
    }
}
```



### 4. input输入框placeholder字体颜色修改

```less
input {
    &::-webkit-input-placeholder { /* WebKit browsers*/ 
        color:#999;
        font-size: 20px;
    }
    &:-moz-placeholder {  /* Mozilla Firefox 4 to 18*/ 
        color:#999;
    }
    &::-moz-placeholder {  /* Mozilla Firefox 19+*/ 
        color:#999;
    }
    &:-ms-input-placeholder { /* Internet Explorer 10+*/ 
        color:#999;
    }
}
```

