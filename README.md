# Fluttify相关项目技术支持方案 

v0.0.1-pre8 by [yohom](https://github.com/yohom)

[English Version](https://github.com/fluttify-project/technical-support-plan/blob/master/README_en.md)

## 基本说明
- 先解决后收费.
- 不解决不收费.
- 已解决不付费拉黑.
- 为了提高效率, 咨询会辅助使用(类似)TeamViewer的工具远程协助方式进行, 请先在本地准备好TeamViewer工具.
- 已确认的工单(bug, 新功能等)会按最高优先级处理, 付费工单内部优先级按时间先后顺序排列.

## 如何发起技术支持请求
- 请在[technical-support-plan](https://github.com/fluttify-project/technical-support-plan/issues/new?assignees=yohom&labels=&template=------.md&title=)仓库*按模板*新建issue来发起技术支持请求.
- 通过各种方式联系到[yohom](https://github.com/yohom), 邮件 yohombao@qq.com, 或者加qq群 938842596.

## 方案
### 咨询
- Fluttify项目咨询: 只要是对我写的代码进行咨询, 那么 ¥100/4个 起付, 4个问题不限时间提问, 也就是说你可以今天问一天问题, 一个月后再问另一个问题.
- 非Fluttify项目咨询: 如果不是我的写的代码, 那么费用依具体情况判定.
- 咨询过程(是否解决, 第几个问题等)将在[technical-support-plan](https://github.com/fluttify-project/technical-support-plan/issues/new?assignees=yohom&labels=&template=------.md&title=)内记录.

### Bug修复
- 根据bug修复难度确认不同的费用.

### 新功能
新功能根据实现复杂度区分价格, 复杂度计算公式:

> 可以直接在method channel传递的类型称为*简单类型*，其他的称为*复合类型*, 具体定义见[Flutter官方文档](https://flutter.dev/docs/development/platform-integration/platform-channels#codec).
> 
> 最终价格 = 基础 ¥100 + (简单参数个数 × 30¥/个) + (简单返回值个数 × 30¥/个) + (复合参数个数 × 50¥/个) + (复合返回值个数 × 50¥/个)
> 
比如现有一个待实现的Dart方法签名如下:

```
(简单返回值)          (复合参数)         (简单参数)
    ↓                    ↓                 ↓
 String exampleMethod(SomeClass object, String string);
```

那么需要:

基础 ¥100 + (简单参数个数1个 × 30¥/个) + (简单返回值个数1个 × 30¥/个) + (复合参数个数1个 × 50¥/个) + (复合返回值个数0个 × 50¥/个) = ¥100 + ¥30 + ¥30 + ¥50 = ¥210

其他类型方法以此类推.

### 业务功能 参考实现/代开发
- 业务功能实现指特定业务场景下的功能组合, 比如微信的发送位置功能, 需要配合搜索插件和地图插件来实现, 本方案提供 参考实现/代开发.

### 新插件开发
- 新插件开发需要先生成插件, 插件生成完成后会上传到[组织](https://github.com/fluttify-project). 后续新功能请求可以走`新功能`方案.
- 插件生成费用为固定价格 ¥1000.

### 悬赏模式
后期条件允许可以开放悬赏模式, 即以上技术支持方案所有人都可以作为支持方参与.

使用者(user)能够快速解决问题, 贡献者(contributor)能够获得报酬, 拥有者(owner)能够持续迭代项目. 这也是我对开源社区健康发展的一个愿景 :) .