### 如图，在文字增加到一定的量时，字体大小会异常
#### 正常的
![](https://lin09.github.io/lssues/images/meta-viewport-initial-scale-0.5-normal.jpg)
#### 异常的
![](https://lin09.github.io/lssues/images/meta-viewport-initial-scale-0.5-error.jpg)

### 解决方法
```
// add css
text-size-adjust: none;
```

* [text-size-adjust](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-size-adjust) | MDN