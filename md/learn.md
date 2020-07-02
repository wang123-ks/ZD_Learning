# 一级标题
## 二级标题
### 三级标题

1. 3213213
1. 312321312
1. 3123123


* 13213213
  * 31232131
  * 321312321
* 13132131 
* 123123123

``` javascript
double i = 10;
/**
* @description 函数说明
**/
function test() { i ++ }
```

``` sh
npm -v
```


> 这是块的说明

`标记`
**加粗**
__下划线__


## 路由
> name path的区别
1. 
1. 
### 动态路由
``` json
{
    path: "/demo/:mapmode",
    component: ShowCase,
    hidden: true,
    name: "demo",
    children: [
      {
        path: ":first/:file",  //动态路由
        name: "codemirror",
        component: () => import("@/views/demo/index"),
      },
      {
        path: ":first/:second/:file",
        name: "codemirror",
        component: () => import("@/views/demo/index"),
      },
    ],
  },```

  svv 