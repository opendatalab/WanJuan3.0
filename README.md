# WanJuan3.0
![](https://github.com/opendatalab/WanJuan3.0/blob/main/readm_pic/Mask%20group-2.png?raw=true)
WanJuan3.0（“万卷·丝路”）一个作为综合性的纯文本语料库，采集了多个国家地区的网络公开信息、文献、专利等资料，数据总规模超1.2TB，Token总数超过300B（300 billion），处于国际领先水平。首期开源的语料库主要由泰语、俄语、阿拉伯语、韩语和越南语5个子集构成，每个子集的数据规模均超过150GB。 
## 下载链接：
1. WanJuan-Thai：万卷-丝路（泰语）https://opendatalab.com/OpenDataLab/WanJuan-Thai
2. WanJuan-Russian：万卷-丝路（俄语）https://opendatalab.com/OpenDataLab/WanJuan-Russian
3. WanJuan-Korean：万卷-丝路（韩语）https://opendatalab.com/OpenDataLab/WanJuan-Korean
4. WanJuan-Vietnamese：万卷-丝路（越南语）https://opendatalab.com/OpenDataLab/WanJuan-Vietnamese
5. WanJuan-Arabic：万卷-丝路（阿拉伯语） https://opendatalab.com/OpenDataLab/WanJuan-Arabic

基于“书生·浦语”智能标签分类体系，上海AI实验室研究团队将每个语料子集细分为7个大类和32个小类，覆盖历史、政治、文化、房产、购物、天气、餐饮、百科、专业知识等多类具有语言所在地特征内容，便于研究者根据具体需求检索数据，并可适应不同研究领域多样化需求。
![]()

“万卷·丝路”语料库通过专家人工标注，确立了包含七个维度的文本数据质量评估体系，从完整性、有效性、可理解性、流畅性、相关性、相似性和安全性等方面保障数据的高标准与高质量。


通过使用基于大语言模型的数据质量评估开源工具——[Dingo](https://github.com/DataEval/dingo)，研究团队从多维度对“万卷·丝路”的数据质量进行了全面评估。结果表明，其五个子集均获得优异的综合评分，显著优于同类语言语料库。

![](http://sh.people.com.cn/mediafile/pic/20250110/9/17589679725858832301.jpg)


为充分体现多语言特色、全面提升数据质量与适用性，发挥实验室领先的数据处理能力优势，研究团队为“万卷·丝路”设计一套精准化数据处理流程：

1.对网页及非网页数据进行标准化处理，统一数据格式，然后运用局部敏感哈希算法高效去重，降低冗余；

2.在安全性处理上，建立域名黑名单筛除不良网页数据，构建多语言特色敏感词表并结合语境评估，精准过滤有害内容，同时训练语言安全模型，进行多维度不良内容检测和筛选；

3.利用主题分类器对数据进行分类，优化知识域分布；

4.通过PPL初筛快速剔除低质量数据，再借助基于BERT的质量分类模型精准筛选高质量内容。

该流程有效融合多语言特点与行业通识技术，为多语言模型训练提供了高质量、安全可靠的数据基础。

![](http://sh.people.com.cn/mediafile/pic/20250110/94/3624188245534375270.png)
万卷·丝路数据处理流程

为评估“万卷·丝路”数据集质量，研究团队使用“万卷·丝路”数据在开源基座上进行继续预训练，实验结果显示，使用“万卷·丝路”后，模型在多语言内容理解及推理能力上的表现均获得了提升。
