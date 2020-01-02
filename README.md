# 身份证号码、法人和其他组织统一社会信用代码 的合法性校验
<div align="center">

[![MIT](https://img.shields.io/dub/l/vibe-d.svg?style=flat-square)](http://opensource.org/licenses/MIT)

</div>

用于校验 `身份证号码` 和 `法人和其他组织统一社会信用代码` 的工具。(基于 <a href="https://github.com/bluesky335/IDCheck" target="_blank">IDCheck</a>，这是JS的实现方式（搬砖手动狗头）)

计算规则参考国家标准文件：

- **标准号：GB 11643-1999**：[公民身份证号码](http://www.gb688.cn/bzgk/gb/newGbInfo?hcno=080D6FBF2BB468F9007657F26D60013E)

- **标准号：GB 32100-2015**：[法人和其他组织统一社会信用代码编码规则](http://www.gb688.cn/bzgk/gb/newGbInfo?hcno=24691C25985C1073D3A7C85629378AC0)

> 注：由于早期部分试点地区推行 `法人和其他组织统一社会信用代码` 较早，会存在部分代码不符合国家标准的情况。但它们都是合法的代码，应当另行处理。
> 例如：
>
> **福建恒跃柳工机械销售有限公司**: `91350100M0001TGQXM` 计算出的校验位是 1 和 M 不符
>
> **厦门云上晴空航空科技有限公司**:`91350211M0000XUF46` 计算出的校验位是 R 和 6 不符
>
> **厦门黑脉网络科技有限公司**`91350203M0001FUE2P` 计算出的校验位是 J 和 P 不符
# 浏览器支持
IE5+和现代浏览器
# 使用方法

```
	<script src="../dist/validators.min.js"></script>
```

- 法人和其他组织统一社会信用代码
```
  if (validators.isUSCI('91350100M000100Y43')) {
	console.log('✅正确')
  } else {
    console.log('✅错误')
  }
```

- 身份证号码

```
  if (validators.isID('91350100M000100Y43')) {
	console.log('✅正确')
  } else {
    console.log('✅错误')
  }
```


# License
[MIT](http://opensource.org/licenses/MIT)
