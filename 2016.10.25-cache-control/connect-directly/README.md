## Cache-Control: max-age=60, must-revalidate

1. 第一次访问：返回`200`
2. 第二次访问，假设距离距离第一次访问的时间
    a、小于等于60秒：`200`，from cache
    b、大于60秒：向源服务器发起请求，如果内容未变化，返回`304`；如果内容变化，返回`200`；

## Cache-Control: no-cache

1. 第一次访问：返回`200`
2. 第二次访问：向源服务器发起请求，如果内容未变化，返回`304`；如果内容变化，返回`200`；