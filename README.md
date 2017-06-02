
## javascript常见封装方法 ##

1、对象字面量简单封装（不完整的模块模式，因为无法达到变量、方法私有效果。不过确实有分离和组织代码的能力，也就算一种简略的模块模式的实现方式）
```javascript
var Carousel = {
    init: function(){...},
    bind: function(){...},
    showPre: function(){...},
    showNext: function(){...}
};
```
2、原型构造器模式封装
```javascript
function Carousel(){
    this.init();
}
Carousel.prototype = {
    init: function(){...},
    bind: function(){...},
    showPre: function(){...},
    showNext: function(){...}
};
```
3、通用写法
```javascript
(function(window,$){
    function Carousel(){};
    Carousel.prototype = {};
    window.Carousel = Carousel;
})(window,jQuery)
```
