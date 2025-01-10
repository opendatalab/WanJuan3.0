# WanJuan3.0
![](https://github.com/opendatalab/WanJuan3.0/blob/main/readm_pic/Mask%20group-2.png?raw=true)
WanJuan3.0（“万卷·丝路”）一个作为综合性的纯文本语料库，采集了多个国家地区的网络公开信息、文献、专利等资料，数据总规模超1.2TB，Token总数超过300B（300 billion），处于国际领先水平。首期开源的语料库主要由泰语、俄语、阿拉伯语、韩语和越南语5个子集构成，每个子集的数据规模均超过150GB。 
## 下载链接：
1. WanJuan-Thai：万卷-丝路（泰语）https://opendatalab.com/OpenDataLab/WanJuan-Thai
2. WanJuan-Russian：万卷-丝路（俄语）https://opendatalab.com/OpenDataLab/WanJuan-Russian
3. WanJuan-Korean：万卷-丝路（韩语）https://opendatalab.com/OpenDataLab/WanJuan-Korean
4. WanJuan-Vietnamese：万卷-丝路（越南语）https://opendatalab.com/OpenDataLab/WanJuan-Vietnamese
5. WanJuan-Arabic：万卷-丝路（阿拉伯语） https://opendatalab.com/OpenDataLab/WanJuan-Arabic

## 主题分类
基于“书生·浦语”智能标签分类体系，上海AI实验室研究团队将每个语料子集细分为7个大类和32个小类，覆盖历史、政治、文化、房产、购物、天气、餐饮、百科、专业知识等多类具有语言所在地特征内容，便于研究者根据具体需求检索数据，并可适应不同研究领域多样化需求。
![](http://sh.people.com.cn/mediafile/pic/20250110/77/8003117310433732061.jpg)

## 数据质量评估
“万卷·丝路”语料库通过专家人工标注，确立了包含七个维度的文本数据质量评估体系，从完整性、有效性、可理解性、流畅性、相关性、相似性和安全性等方面保障数据的高标准与高质量。
<table>
  <tr>
    <th>序号</th>
    <th>一级分类</th>
    <th>二级分类</th>
    <th>定义</th>
  </tr>
  <tr>
    <td>1</td>
    <td rowspan="5">质量类</td>
    <td>完整性</td>
    <td>数据内容是否语义完整</td>
  </tr>
  <tr>
    <td>2</td>
    <td>有效性</td>
    <td>数据内容是否含有效的语义内容</td>
  </tr>
  <tr>
    <td>3</td>
    <td>可理解性</td>
    <td>数据内容是否因格式等错误导致语义有歧义不可理解</td>
  </tr>
  <tr>
    <td>4</td>
    <td>流畅性</td>
    <td>数据内容语义是否流畅</td>
  </tr>
  <tr>
    <td>5</td>
    <td>相关性</td>
    <td>数据是否有上下文主题不相关内容</td>
  </tr>
  <tr>
    <td>6</td>
    <td>重复类</td>
    <td>相似性</td>
    <td>数据是否重复</td>
  </tr>
  <tr>
    <td>7</td>
    <td>安全类</td>
    <td>安全性</td>
    <td>数据是否涉及内容安全</td>
  </tr>
</table>

通过使用基于大语言模型的数据质量评估开源工具——[Dingo](https://github.com/DataEval/dingo)，研究团队从多维度对“万卷·丝路”的数据质量进行了全面评估。结果表明，其五个子集均获得优异的综合评分，显著优于同类语言语料库。

![](http://sh.people.com.cn/mediafile/pic/20250110/9/17589679725858832301.jpg)


## 数据处理流程
为充分体现多语言特色、全面提升数据质量与适用性，发挥实验室领先的数据处理能力优势，研究团队为“万卷·丝路”设计一套精准化数据处理流程：

1.对网页及非网页数据进行标准化处理，统一数据格式，然后运用局部敏感哈希算法高效去重，降低冗余；

2.在安全性处理上，建立域名黑名单筛除不良网页数据，构建多语言特色敏感词表并结合语境评估，精准过滤有害内容，同时训练语言安全模型，进行多维度不良内容检测和筛选；

3.利用主题分类器对数据进行分类，优化知识域分布；

4.通过PPL初筛快速剔除低质量数据，再借助基于BERT的质量分类模型精准筛选高质量内容。

该流程有效融合多语言特点与行业通识技术，为多语言模型训练提供了高质量、安全可靠的数据基础。

![](http://sh.people.com.cn/mediafile/pic/20250110/94/3624188245534375270.png)


## 模型验证
为评估“万卷·丝路”数据集质量，研究团队使用“万卷·丝路”数据在开源基座上进行继续预训练，实验结果显示，使用“万卷·丝路”后，模型在多语言内容理解及推理能力上的表现均获得了提升。


## 许可
WanJuan3.0（万卷·丝路）整体采用CC BY 4.0许可协议。您可以自由共享、改编该数据集，唯需遵循以下条件：

署名：您必须适当地标明作者、提供指向本协议的链接，以及指明是否（对原始数据集）做了修改。您可以以任何合理的方式这样做，但不能以任何方式暗示许可人同意您或您的使用。 没有附加限制：您不得使用法律条款或技术措施来限制他人执行许可证允许的任何操作。 完整协议内容，请访问CC BY 4.0协议全文。

## 特别注意事项
请注意，本数据集的某些子集可能受制于其他协议规定。在使用特定子集之前，请务必仔细阅读相关协议，确保合规使用。更为详细的协议信息，请在特定子集的相关文档或元数据中查看。

OpenDataLab作为非盈利机构，倡导和谐友好的开源交流环境，若在开源数据集内发现有侵犯您合法权益的内容，可发送邮件至（OpenDataLab@pjlab.org.cn），邮件中请写明侵权相关事实的详细描述并向我们提供相关的权属证明资料。我们将于3个工作日内启动调查处理机制，并采取必要的措施进行处置（如下架相关数据）。但您应确保您投诉的真实性，否则采取措施后所产生的不利后果应由您独立承担。

## 引文
```
@misc{he2024opendatalabempoweringgeneralartificial,
      title={OpenDataLab: Empowering General Artificial Intelligence with Open Datasets}, 
      author={Conghui He and Wei Li and Zhenjiang Jin and Chao Xu and Bin Wang and Dahua Lin},
      year={2024},
      eprint={2407.13773},
      archivePrefix={arXiv},
      primaryClass={cs.DL},
      url={https://arxiv.org/abs/2407.13773}, 
}
```
