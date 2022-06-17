# CSS3动画相关笔记

## transition属性
transition属性用于设置四个过渡属性：

transition-property过渡效果的CSS属性的名称（height、width、opacity以及transform属性等）；

transition-duration完成过渡效果需要时间；

transition-timing-function规定速度效果的速度曲线；

transition-delay过渡效果何时开始（延迟时间）

```css
/* fade-transform */
.fade-transform-leave-active,
.fade-transform-enter-active {
  transition: all .25s;
}

.fade-transform-enter {
  opacity: 0;
  transform: translateX(-10px);
}

.fade-transform-leave-to {
  opacity: 0;
  transform: translateX(10px);
}
```
**本质上transition是通过监测页面上一个元素的属性变化来实现动画的，需要注意的是所有元素都默认带有各种属性，如元素默认带有透明度opacity（默认为1），而不是设置元素之后加上opacity词条**
