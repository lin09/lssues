# postcss-pxtorem 无效
## 解决方法
* 必需加`"propList": ["*"]`
```
  "postcss": {
    "plugins": {
      "postcss-pxtorem": {
        "propList": ["*"]
      }
    }
  }
```