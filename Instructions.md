利用[allcontributors-bot](https://allcontributors.org/docs/en/bot/installation)实现contributors table
主要步骤如下：
1.  [安装Bot](https://allcontributors.org/docs/en/bot/installation)
2.	在需要展示贡献表的文件（README.md 与README_CN.md文件）的段落中添加如下语句：
```
<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
```

3.	在issue或者pr中进行评论，格式为：
```
@all-contributors please add @<username> for <contributions>
```
如：@all-contributors please add @wanhanbo for code
@<username>是贡献者昵称
<contributions>是[贡献类型](https://allcontributors.org/docs/en/emoji-key)

 Bot将自动创建 .all-contributorsrc 文件，可以在其中任意修改配置。
 
 ### 其他注意事项
 * 必须在files中增加 "README_CN.md"保证中文版readme的更新
 * 首次使用后，需要删除readme文件中bot自己增加的两个部分
   分别是：开头增加的badge部分 
 ```
 <!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-3-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
 ```
 以及最后增加的 contributors部分。  
 这两个部分可以在我们的主体内容中自己设计，用bot的会带来格式上的错误。
