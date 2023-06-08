at design system

### 本地开发

执行 `npm run site`，参考 docs/publish.md 文档操作。

### 本地构建

执行 `npm run build`

### 发布正式版

`def p -d`，日常CDN发布

`def p -o`，线上CDN发布

`npm run pub`，npm发布

如果出现 402 未授权报错问题，执行 `npm publish --access public`

### 发布测试版

*测试版不要发 def！* 因为发 def 会自动 merge 到 master 上

`rm -rf node_modules`
`tnpm i`
`npm run build`
`npm version x.x.x-alpha.x`
`npm publish --tag {{你的测试版本号}}`


### 发布后

- 基于上一个分支新建下一版本的 daily/x.x.x 分支
- npm version patch //默认更新最后一位
- git push
