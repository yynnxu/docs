# 特性支持类

`特性优势` `端侧推理` `功能模块` `推理工具`

<a href="https://gitee.com/mindspore/docs/blob/master/docs/faq/source_zh_cn/supported_features.md" target="_blank"><img src="./_static/logo_source.png"></a>

Q：MindSpore有量化推理工具么？

A：[MindSpore Lite](https://www.mindspore.cn/lite)支持云侧量化感知训练的量化模型的推理，MindSpore Lite converter工具提供训练后量化以及权重量化功能，且功能在持续加强完善中。

<br/>

Q：MindSpore并行模型训练的优势和特色有哪些？

A：MindSpore分布式训练除了支持数据并行，还支持算子级模型并行，可以对算子输入tensor进行切分并行。在此基础上支持自动并行，用户只需要写单卡脚本，就能自动切分到多个节点并行执行。

<br/>

Q：请问MindSpore实现了反池化操作了吗？类似于`nn.MaxUnpool2d` 这个反池化操作？

A：目前 MindSpore 还没有反池化相关的接口。如果用户想自己实现的话，可以通过自定义算子的方式自行开发算子,自定义算子[详见这里](https://www.mindspore.cn/tutorial/training/zh-CN/master/advanced_use/custom_operator_ascend.html)。

<br/>

Q：MindSpore有轻量的端侧推理引擎么？

A：MindSpore轻量化推理框架MindSpore Lite已于r0.7版本正式上线，欢迎试用并提出宝贵意见，概述、教程和文档等请参考[MindSpore Lite](https://www.mindspore.cn/lite)

<br/>

Q：MindSpore在语义协同和处理上是如何实现的？是否利用当前学术界流行的FCA理论？

A：MindSpore框架本身并不需要支持FCA。对于语义类模型，用户可以调用第三方的工具在数据预处理阶段做FCA数学分析。MindSpore本身支持Python语言，`import FCA`相关包即可使用。

<br/>

Q：当前在云上MindSpore的训练和推理功能是比较完备的，至于边端场景（尤其是终端设备）MindSpore有什么计划？

A：MindSpore是端边云统一的训练和推理框架，支持将云侧训练的模型导出到Ascend AI处理器和终端设备进行推理。当前推理阶段支持的优化包括量化、算子融合、内存复用等。

<br/>

Q：MindSpore自动并行支持情况如何？

A：自动并行特性对CPU GPU的支持还在完善中。推荐用户在Ascend 910 AI处理器上使用自动并行，可以关注开源社区，申请MindSpore开发者体验环境进行试用。

<br/>

Q：MindSpore有没有类似基于TensorFlow实现的对象检测算法的模块？

A：TensorFlow的对象检测Pipeline接口属于TensorFlow Model模块。待MindSpore检测类模型完备后，会提供类似的Pipeline接口。

<br/>

Q：其他框架的脚本或者模型怎么迁移到MindSpore？

A：关于脚本或者模型迁移，可以查询MindSpore官网中关于[网络迁移](https://www.mindspore.cn/tutorial/training/zh-CN/master/advanced_use/migrate_3rd_scripts.html)的介绍。

<br/>

Q：MindSpore是否附带开源电商类数据集？

A：暂时还没有，可以持续关注[MindSpore官网](https://www.mindspore.cn)。
