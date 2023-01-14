title: '[2020-02-25]SSL搞到啦！顺便弄了一下强制https'
author: Eicy
tags:
  - 站点
categories:
  - 碎碎念
date: 2023-01-14 09:44:00
---
今天宣传被人刺激了

A:你这博客做的挺好。

我:谢大佬夸奖！

A:可是没有SSL，被我拉黑了。

我:我马上！

然后我打开了久违的网站

	freessl.cn

本来看到FSL上有一键部署，但是我下载下来，

嗯，不会。

还是原来的配方，证书申请下来反反复复在DA后台输入好几遍
格式是这样的

先输入私钥，再输入CA证书

然后我就想http直接跳转到https，但是我在DA整的301重定向hhh

然后重定向次数过多hhhhhhh

我就想起来以前ELF是怎么强制https的

对.htaccess 万恶之源

输入

	RewriteCond %{SERVER_PORT} !^443$
	RewriteRule ^(.*)?$ https://%{SERVER_NAME}/$1 [L,R]

就行了