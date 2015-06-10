在angularjs不同的视图直接进行切换时，service之间的状态订正非常容易出错。目前学习到比较好的方案是：
- service里面增加reset方法，视图在发生转换的时候进行数据重置。
- 不要太多依赖rootscope，否则数据很容易乱掉。
- 多个视图之间共用的组件抽取成directive