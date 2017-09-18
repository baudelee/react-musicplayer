### 项目后续更新
* Todos:上传gh-pages,gif截图,修改markdownToHtml项目的markdown

* 将项目整体由create-react-app迁移到手动构建的webpack环境
* 引入图片时，如img标签，最好使用相对路径，因为无法确定项目最终会放在哪个服务器下面。在css中通过background属性引入图片时，url()中的相对路径是相对于该文件本身，而在less文件中是相对于打包后文件所被引入的html文件
* 当browserHistory被用在前端时，在服务器上有一个告诫，如果用户开始他们在example.com上的访问，然后导航到/users，React Router会像期待的那样处理这种场景，但是当用户直接通过在浏览器中键入example.com/users或者在example.com/users上刷新来开始他们的访问，那么浏览器会发起一次为/users对服务器的请求，但是如果这不是一个服务器端的路由器，就会得到一个404的错误。比如本项目直接在本地运行展示的话，无法访问，如果放在服务器下，index.html是在服务器的根路径下，可以访问，但仍有上面提到的问题，若不在服务器的根路径下，会报错，为了能在gh-pages上演示，只能换成hashHistory
* box-sizing:默认值为content-box，width只包含内容宽度，border-box包含padding和边框宽度
* box-shadow:阴影类型（可选值，默认外阴影outset,可设为inset) 水平偏移量 垂直偏移量 阴影模糊半径(可选) 阴影模糊距离（可选）阴影颜色（可选） 
* 动画 animation:name(keyframe名称) duration(完成一次动画的时间) timing-function(规定动画的速度曲线) delay(规定动画开始之前的延迟) iteration-count(规定动画播放的次数) direction(规定是否轮流反向播放动画)
* infinite 规定动画无限次播放
* animation-play-state:paused（暂停动画）
* 关键帧 @keyframes name{
    from {属性：初始值}
    to {属性：末值}
}
* transform 转换属性,rotate(angle)，定义2D旋转
* Z-index 仅在定位元素上生效，默认值（auto）
* filter 滤镜，定义元素的可视效果（例如：模糊和饱和度），blur(px)给图像设置高斯模糊。
* background-size:cover（把背景图像扩展至足够大，以使背景图像完全覆盖背景区域）