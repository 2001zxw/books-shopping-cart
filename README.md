# books-shopping-cart
## 项目描述
本项目是在学习了一小部分Vue的基础，所做的一个小练习
## 运用的方法库和框架
Vue3.0；
bootstrap@3
## 项目介绍
页面展示数据的相关信息，通过点击按钮可以进行一些操作
## 项目亮点
1. 当图书数量为1时，不能再点击减号按钮，点击效果也消失；
2. 重置按钮会将数量重置为 1；
3. 点击删除按钮时，弹出‘删除成功’的提示框；
4. 当图书全部删除时，弹出 ‘您的购书车空空如也~’的提示，并且表格的总价一行消失；

## 项目难点
如何判断表格中的书全部被删除后，弹出‘您的购书车空空如也~’的提示，并且表格的总价一行消失的功能。
## 解决方案
在data() 方法中写一个seen()方法进行判断，判断books这个数组的长度为0时，表格中的书就全部被删除了；
seen()方法: return this.books.length===0?true:false；
在空空如也这个提示框 的div上添加 v-show = "seen()",表格中的书就全部被删除后显示；
在表格的总价一行添加 v-show = "!seen()" ,通过取反，就可以解决了。

## 项目收获
1. 巩固了当天的所学；
2. 对 v-show 加深了理解。
