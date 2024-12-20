## CC-Plugin支持AssetDB的示例工程



creatorv2/v3的插件是支持携带代码并被项目引用的，cc-plugin同样也适配了，只需要在`cc-plugin.config.ts`如下配置
```ts
const manifest: CocosPluginManifest = {
    // ...
    asset_db_v2:{path:'./code-v2'},
    asset_db_v3:{path:'./code-v3'}
}
```

在cc-plugin的工程代码中编写对应的代码即可

- code-v2
  - hello.ts
- code-v3
  - hello.ts
- cc-plugin.config.ts

具体的细节，cc-plugin会自动帮你处理，好处是只需要一个工程，就能同时适配v2/v3版本的creator，维护起来更加方便简单。

[了解具体细节](https://juejin.cn/spost/7450035463769014272)