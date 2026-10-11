# 实验2 HTML5进阶综合训练 — 用户注册页面
Web应用开发技术实验作业

## 作业内容
制作用户注册网页，综合练习**表单、列表、表格、HTML5新表单控件、JS表单数据捕获**。
1. 使用语义化标签 `<header>`、`<main>`、`<footer>`搭建页面整体结构。
2. 实现完整注册表单：用户名、密码、确认密码、性别单选、出生日期、邮箱、手机号、兴趣多选、头像上传、城市下拉、个人简介，包含提交、重置按钮。
3. 使用`required`实现必填校验，`pattern`实现手机号11位数字正则校验。
4. JS监听表单submit事件，阻止默认提交，把表单收集到的数据打印到浏览器Console控制台。
5. 页面加入表格（带单元格合并colspan）、无序列表ul、有序列表ol、定义列表dl。

## 使用标签与知识点
- HTML语义标签：header、main、footer
- 表单：form、input(text/password/radio/checkbox/file/date/email/tel)、select、option、textarea、button、label
- 列表：ul、ol、dl、dt、dd
- 表格：table、thead、tbody、tr、th、td，colspan单元格合并
- 属性：name、required、pattern、placeholder、checked、selected、multiple、accept
- JavaScript：addEventListener、FormData，阻止表单默认提交`e.preventDefault()`
- CSS：外部样式表style.css，美化页面基础样式

## 文件清单
- index.html：注册页面主html文件
- style.css：外部CSS样式文件
- README.md：本说明文档

## 运行环境
开发工具：VS Code
预览工具：Live Server插件，Chrome / Edge浏览器
调试：F12开发者工具，Elements查看DOM，Console查看表单输出数据

## 遇到的问题以及解决方法
1. 问题：表单提交之后页面会刷新，控制台拿不到数据。
解决：JS事件回调中写`e.preventDefault()`阻止浏览器表单默认跳转提交行为。

2. 问题：input控件没有name属性，FormData获取不到表单值。
解决：给每一个需要提交的表单控件补上name属性。

3. 问题：打开网页样式没有生效。
解决：检查link引入外部css的路径，确认html和css在同一个文件夹，保存文件刷新浏览器。

## 运行方式
用Live Server打开index.html，填写注册信息，点击注册按钮，打开F12控制台即可看到收集的表单JSON数据。

> 注意：本项目仅前端演示，没有后端服务器，数据只存在浏览器控制台，刷新页面数据丢失。