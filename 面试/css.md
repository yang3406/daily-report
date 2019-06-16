##### 什么是BFC? 有什么特征
> 一:BFC(块格式化上下文),可以理解为他是一个独立的容器,它的box布局和外面的box容器布局不相关(包括父级和兄弟级的元素)。
二:怎么才能形成BFC? 
1:float的值不能为none
2:overflow的值不能为visible
3:display的值为table-cell,table-caption,inline-block中的一个
4:position的值不为static,relative;
例如1：float父级坍塌.解决
例如2:外边距坍塌,避免块级元素外边距合并的问题,margin-top-bottom上下会合并
解决:1:设置父级元素为overflow:auto(创建一个新的FFC,包含浮动)2:设置一个新的display属性:flow-root,创建无副作用的BFC，它会把内部所有的内容都会参与BFC.浮动的元素不会从底部溢出