# postcss-pxtorem 无效

## 解决方法
* 必需配置 propList ，详细配置查看 [postcss-pxtorem](https://github.com/cuth/postcss-pxtorem)

```
  "postcss": {
    "plugins": {
      "postcss-pxtorem": {
        "propList": ["*"]
      }
    }
  }
```