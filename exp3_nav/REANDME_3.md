# 实验3 CSS布局实战——导航菜单
Web应用开发技术实验作业

## 作业内容
编写HTML+CSS实现两级导航菜单页面，不修改原有HTML结构，仅通过CSS完成样式设置。
1. 一级菜单.html：使用table标签制作水平一级导航菜单，鼠标悬浮菜单项，背景颜色改变。
2. 二级菜单.html：ul、li列表实现下拉二级导航，使用flex布局实现一级菜单横向排列；利用position相对定位+绝对定位，鼠标悬浮一级菜单“教学院(部)”，弹出二级下拉子菜单。

## 使用到的知识点
- HTML：table、ul、li、a超链接标签
- CSS：flex弹性布局、position定位（relative、absolute）、:hover伪类选择器
- 样式：清除列表默认内外边距、清除列表圆点、超链接去掉下划线

## 遇到的困难及解决办法
1. **问题**：二级下拉菜单会把下方页面内容挤下去
原因：二级菜单没有脱离文档流，还占用页面空间
解决：给二级ul设置`position:absolute`，父级li设置`position:relative`作为定位参照，让子菜单悬浮弹出。

2. **问题**：ul、li自带默认间距与列表黑点，页面排版错乱
解决：使用通配选择器`*`统一清除margin、padding，设置`list-style:none`去掉列表圆点。

## 文件清单
- 一级菜单.html：一级水平导航页面
- 二级菜单.html：带下拉效果的二级导航页面

## 实验环境
开发工具：Visual Studio Code
预览工具：Live Server插件，Edge浏览器查看运行效果