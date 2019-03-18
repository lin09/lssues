# vue-cli-3 创建项目选择 yarn 安装依赖包出现的问题
## 环境
* Vue CLI v3.5.1
* yarn install v1.15.2
* node v10.15.3
* npm 6.4.1

## 问题
* There appears to be trouble with your network connection. Retrying...
  * 分析
    * yarn 使用“npm源”或“淘宝源”在没设置代理时都出现
    * 这是网络环境问题
  * 解决方法
    * 设置“代理 + npm源”（不可使用淘宝源）

* error http://registry.npm.taobao.org/@types/events/download/@types/events-3.0.0.tgz: Integrity check failed for "@types/events" (computed integrity doesn't match our records, got "sha1-mgoN+vYok9krh1uPJpjKQRSXPog=")
  * 分析
    * yarn 使用“淘宝源”（没设置代理）
    * 新版本的 yarn 要校验 offline cache 的完整性
    * 淘宝 npm 源没有提供「完整性」（integrity）这一字段
  * 解决方法
    * 设置“代理 + npm源”（不可使用淘宝源）

## yarn 代理设置
```
yarn config set proxy http://localhost:1080
yarn config set https-proxy http://localhost:1080
```
### 查看配置
```
yarn config list
npm config list
```