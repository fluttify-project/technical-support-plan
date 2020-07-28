# Fluttify相关项目技术支持方案 

v0.1.0 by [yohom](https://github.com/yohom)

[English Version](https://github.com/fluttify-project/technical-support-plan/blob/master/README_en.md)

## 如何发起技术支持请求
- 请在[technical-support-plan](https://github.com/fluttify-project/technical-support-plan/issues/new?assignees=yohom&labels=&template=------.md&title=)仓库*按模板*新建issue来发起技术支持请求.
- 通过各种方式联系到[yohom](https://github.com/yohom), 邮件 yohombao@qq.com, 或者加qq群 938842596.

## 方案

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

其他类型方法以此类推. *如果一个非简单参数为简单参数的封装类, 那么按封装前的简单参数来计算*.

### 新插件开发
- 新插件开发需要先生成插件, 插件生成完成后会上传到[组织](https://github.com/fluttify-project). 后续新功能请求可以走`新功能`方案.
- 插件生成费用为固定价格 ¥1000.
