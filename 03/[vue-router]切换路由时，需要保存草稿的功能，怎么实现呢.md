# 切换路由时，需要保存草稿的功能，怎么实现呢

- beforeRouteLeave
```js
beforeRouteLeave (to, from, next) {
  if(用户已经输入信息){
    //出现弹窗提醒保存草稿，或者自动后台为其保存
    
  }else{
    next(true);//用户离开
  }
}
```

- keep-alive 缓存那个路由
