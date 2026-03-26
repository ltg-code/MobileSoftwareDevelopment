\# Jetpack Compose 电子名片实验报告

\- 姓名：陈邦国

\- 学号：2025003014

\- 开发环境：Android Studio + Kotlin + Jetpack Compose



\## 一、名片展示的个人信息

1\. 头像：Android Logo

2\. 姓名：陈邦国

3\. 职位：Android 开发工程师

4\. 联系方式：2025003014

5\. 社交账号：@chenbangguo

6\. 邮箱：chenbangguo@school.com



\## 二、布局结构说明

本项目使用 Jetpack Compose 声明式 UI 构建界面，整体布局采用垂直容器与水平容器组合实现。



\### 使用的 Composable 组件

\- Column：垂直布局，用于整体页面、个人信息区、联系方式区

\- Row：横向布局，用于实现“图标+文字”的联系方式行

\- Image：展示头像图片

\- Text：显示姓名、职位、联系方式等文本

\- Icon：显示 Material 图标（电话、分享、邮件）

\- Spacer：控制组件之间的间距

\- Modifier：设置大小、边距、背景、对齐方式



\### 布局层次

1\. 最外层：Column 铺满屏幕，设置背景色

2\. 上半部分 CardTop：Column 嵌套 Image + Text，展示头像、姓名、职位

3\. 下半部分 CardBottom：Column 包含多个 ContactRow

4\. 联系方式行 ContactRow：Row 横向排列 Icon + Text



\## 三、遇到的问题与解决方法

\### 问题1：Unresolved reference: drawable

\- 原因：未正确导入项目 R 类，图片资源无法识别

\- 解决：导入包名对应的 R 文件，将图片放入 drawable 目录，同步 Gradle



\### 问题2：Material Icons 图标无法使用

\- 原因：缺少图标导入语句

\- 解决：添加 Icons.Default.Phone / Share / Email 相关导入



\### 问题3：界面排版不居中、布局错乱

\- 原因：未设置水平对齐与合理间距

\- 解决：使用 horizontalAlignment 居中，配合 Spacer 和 padding 调整布局



\## 四、实验总结

本次实验完成了 Jetpack Compose 电子名片界面开发，掌握了 Column、Row、Image、Text、Icon、Modifier 等基础组件的使用，理解了声明式 UI 的构建方式，能够独立完成界面布局与常见错误处理。

