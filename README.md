# uniapp

## Project setup
```
// 安装
yarn install

// 或者
npm install
```

### Compiles and hot-reloads for development
```
// 运行
yarn serve
// 或者
npm run serve
```

### Compiles and minifies for production
```
yarn build

// 或者
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


运行\发布 uni-app
```
npm run dev:%PLATFORM%
npm run build:%PLATFORM%
```

**%PLATFORM%** 可取值如下：

| 值        | 平台                |
| --------- | ------------------- |
| app-plus  | app平台生成打包资源 |
| h5        | H5                  |
| mp-weixin | 微信小程序          |
| mp-alipay | 支付宝小程序        |


## common
该文件夹中包含着一些通用的逻辑和css文件

## components
该文件夹中包含着一些uniapp通用的ui组件，可供多平台使用。

## hybird/html

打包成h5页面的首页，可不做处理。

## pages
包含我们需要的组件以及UI用例等。

### about
关于的页面

### component
component tab页面

### API
接口 tab页面

### extUI

扩展tab页面

### template

模板tab页面

### 数据请求模板
```
tologin(provider) {
    uni.login({
        provider: provider.id,
        // #ifdef MP-ALIPAY
        scopes: 'auth_user', //支付宝小程序需设置授权类型
        // #endif
        success: (res) => {
            console.log('login success:', res);
            // 更新保存在 store 中的登录状态
            this.login(provider.id);
        },
        fail: (err) => {
            console.log('login fail:', err);
        }
    });
}
```

## platforms/app-plus

iOS和android平台的依赖的东西

## static

静态图片资料

## store

统一数据管理
类似以vuex

## wxcomponents/vant

微信组件


## 如何以微信小程序打开

```
npm run dev:mp-weixin

// Compiled successfully

// DONE  Build complete. The dist/dev/mp-weixin directory is ready. Watching for changes...

导入uniapp下的dist/dev/mp-weixin即可

```

