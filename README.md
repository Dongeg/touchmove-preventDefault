# touchmove-preventDefault
移动端禁止拖动事件
方法一
```js
  var handle=function (e) {
    e.preventDefault();
  }
  //显示大图时禁止页面拖动
  function show_big_img(obj) {
    document.addEventListener("touchmove",handle, false);
  }
  //大图隐藏时恢复拖动
  function hide_big_img() {
    document.removeEventListener("touchmove",handle, false);
  }

```

方法二
```js
  var body=document.getElementsByTagName("body")[0];
  //显示大图时禁止页面拖动
  function show_big_img(obj) {
    body.style.position="fixed";
  }
  //大图隐藏时恢复拖动
  function hide_big_img() {
    body.style.position="inherit";
  }
```
