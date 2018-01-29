# 在页面上需要将一个URL转为二维码并配上文字说明，并提供一个下载按钮，可以下载带有文字说明的二维码图片，效果如下：
<br>

![效果.jpg](http://upload-images.jianshu.io/upload_images/3888312-c7d4f634677f6e08.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

如果说只要一个二维码图片，Github上的[qrcodejs](https://link.juejin.im?target=https%3A%2F%2Fgithub.com%2Fdavidshimjs%2Fqrcodejs)库就能实现；

但是如果再加上文字说明，情况就变得稍微复杂：

1. 直接在canvas里绘画文字，但是canvas里文字不会换行，虽然可以通过js控制每行文字的数量来换行，但是文字有宽有窄，不是一个好的解决方案；

2. svg可以将div整个画出来，再导入到canvas里。这时候二维码和文字说明都在一张canvas里，而且文字实际上可以用css的样式来控制。
但是在最后一步，将canvas转换为base64再导出图片的时候栽了跟头，在canvas里用svg画出来的部分最后转为图片的时候不会呈现。

3. 最后在Github发现了[html2canvas](https://link.juejin.im?target=https%3A%2F%2Fgithub.com%2Fniklasvh%2Fhtml2canvas)这个神奇的库，它可以将一个div绘画成canvas。

<br>
我觉得这个功能挺实用，下载学习了一下
<br>
原文链接：https://juejin.im/post/5a6b3fa051882573485a2d89



