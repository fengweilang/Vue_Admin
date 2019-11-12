# 基于Vue的后台项目管理系统Demo
功能为：增删查改，并用JSONSERVER进行本地的模拟API借口

**用户管理系统**
主要用到Bootstrap进行简单UI设计

1.数据渲染

安装Vue-resource进行数据请求，使用v-for遍历数据，接受返回的值，显示在页面中。

2.增加用户信息

在header添加用户按钮，进入添加页面，输入信息，点击添加

在componets里添加Add组件，ruter-link跳转到Add页面，在页面里分别填入个人信息：姓名、电话、邮箱、学历、毕业学校、职业、个人简介，点击添加按钮，提交表单，表单里的一个默认事件将数据post到JSONSERVER，并把填写的信息组装成一个对象的格式。

3.用户信息管理（增删查改）

在主页信息中添加详情按钮，进入详情页面，可以查看个人信息详情，病有编辑和删除按钮进行相关操作；当你点击详情按钮时，传入一个用户的id值来进入点击某个用户的个人信息，当你的路径动态绑定了参数时path:'/custorm/:id'，components:Detail要获得点击的id值：this.$route.params.id

4.弹出警告框alert

在componets里添加Alert组件，父传子props，动态为子组件传值query:{alert:"用户信息添加成功！"}


