
https://juejin.im/post/5d124a12f265da1b9163a28d?utm_source=gold_browser_extension

1:new的实现原理 是什么?
https://warjiang.github.io/devcat/2016/05/12/JS%E4%B8%ADnew%E5%88%B0%E5%BA%95%E5%8F%91%E7%94%9F%E4%BA%86%E4%BB%80%E4%B9%88/
__proto__ 是原型,prototype是函数默认的一个属性,它指向一个对象,这个对象的constructor属性指向函数本身.
var c = new Foo();步骤分解
var c = new Object();
c.__proto__ = Foo.prototype;
Foo.call(c);