## 介绍
html很适合静态的文档编写，但是当我们做动态的web页面时html本身的标签就支持的很不够了。Angularjs扩展了很多html标签，同时定义了一套机制让开发者自定义标签来开发web程序(同时提供了一个完整的mvc框架)。使用angularjs可以编写出可读性强、开发效率高、内嵌丰富的应用。非常适合crud类型的页面！    

有javaweb开发经验的使用angularjs会感觉非常亲切，可以把angularjs与java的web框架做各种类比（这样比较后会变得非常容易理解）。
## helloWord
- 一般web页面开发过程
    - vm：从contxt上下文种获取数据利用vm语法渲染上。页面到达浏览器后就没有数据了，要重新用js构造数据上下文。
    - json：js在获取数据后，将数据渲染到dom中，监听button等事件后，从dom读取更新后的数据
- angularjs 页面开发过程
    - https://angularjs.org/

## 技术点
- mvc 框架


    前端的mvc框架有很多，最熟悉的有extjs，相比于extjs，angularjs封装了一个更规范完整的mvc逻辑。一个angularjs页面有以下几个关键元素组成：**ng-app**(angularjs声明)；**ng-controller**(控制器声明)；**service(带有query方法的javabean)**。app.js中会声明app、controller、service。

    一个完整的mvc例子，angular-route： 1）index.html中定义应用入口和页面框架（header、body、footer *类似于webx里面的layout*）。2）partials目录下定义了所有的视图(子页面，*类似于webx里的screen*)。3）在app.js：声明应用、配置视图和controller的路由关系（*类似于web.xml?*）。4）controller.js：定义了所有的controller(类似于webx中java层的screen层)。注意啊注意：angularjs是由声明周期的，而webx里的每个screen里没有声明周期，这点很重要。

- controller
    controller里定义了每个子页面的业务逻辑，如：数据加载、异步请求、数据订正。
- directive
    指令，可以理解成jsp里面的tag或者vm里面的vmtool。这里面可以：1）定义html上需要使用的一些公共组件（导航等），2）需要有js交互的视觉组件，3）directive有自己的scope（可以和使用方进行绑定）
- service
    没有用到。。 
- scope
    非常重要，整个angularjs执行的上下文，1）html可以通过ng-model读取scope的数据并进行双向绑定；2）scope有继承关系，app层面是rootScope，具体到controller是继承自app的rootScope
- 内置directive
    - ng-model({{}})：html中读取scope并进行数据绑定的
    - ng-repeat：循环一个scope上的集合数据渲染html
    - http：ajax封装
    - timeout：异步任务
- 常用的directive
    - ui-grid：表格组件
    - pagination：分页组件
    - form(使用bootstrap+ng-model组合)：表单
- 双向绑定原理（不好讲啊啊）：http://www.angularjs.cn/A0a6



## 好用的地方
- 双向数据绑定(不用操作dom)：最常用的是绑定在form表单上，然后controller不用读取dom直接
- directive
- scope
- ui-angular
    - ui-grid
    - pagination
    
    
## 案例
- 后台案例：
    - 开发tip
        - 服务层(java)
        - 页面层(angularjs)
- H5页面案例（讲讲H5页面？）  

## 以后的考虑
- angularjs2
- react-native