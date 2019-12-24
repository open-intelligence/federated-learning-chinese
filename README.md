## 【翻译】联邦学习进展与开放问题

本项目用于[Advances and Open Problems in Federated Learning](https://arxiv.org/abs/1912.04977)文章的翻译，以及对翻译过程中涌现的**概念**和**命题**的解释。

### 人员与分工

- 有意参加的找陈鼎报名，明确投入的精力和时间节点
- 使用github作为协同工具
- 定期meeting并及时上传各自负责的部分

### 目录结构
```
├── chapters
│   ├── 00-abstract.md  					# 摘要
│   ├── 01-introduction.md  				# 引言
│   ├── 02-core_assumptions.md			# 核心假设
│   ├── 03-efficiency_and_effectiveness.md	# 性能和效率
│   ├── 04-privacy.md					# 数据隐私
│   ├── 05-robustness.md					# 防攻击和容错
│   ├── 06-fairness.md					# 公平性
│   ├── 07-conclusion.md					# 总结
│   ├── 08-appendix_a.md				# 附录A
│   └── 09-appendix_b.md				# 附录B-我们觉得一些额外重要的东西
├── docx
├── images
├── README.md
└── templates
    └── docx-template.docx
```
### 格式要求

1. 图片放置在`images/chapter*/`目录下，图片的文件名不能有空格，插入图片时使用**相对路径**（如../images/chapter01/arch.png），而不是全路径
2. 文件格式使用markdown格式，推荐使用typora编辑器
3. 每章按一级、二级、三级目录进行组织，编排同原文

### 讨论

* 通过issue记录讨论的过程

### Word生成

使用pandoc自动生成word，命令：

```bash
pandoc --highlight-style haddock  \
--reference-doc=./templates/docx-template.docx \
01.md  \
02.md  \
-o pandoc.docx
```

pandoc的安装：如果安装了anaconda，使用conda install pandoc后即可完成安装；否则参考<https://pandoc.org/installing.html> 
