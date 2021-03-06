﻿# Supported Operators

`Ascend` `GPU` `CPU` `Environmental Setup` `Beginner` `Intermediate` `Expert`

<a href="https://gitee.com/mindspore/docs/blob/master/docs/faq/source_en/supported_operators.md" target="_blank"><img src="./_static/logo_source.png"></a>

Q: When the `Tile` module in operations executes `__infer__`, the `value` is `None`. Why is the value lost?

A: The `multiples input` of the `Tile` operator must be a constant. (The value cannot directly or indirectly come from the input of the graph.) Otherwise, the `None` data will be obtained during graph composition because the graph input is transferred only during graph execution and the input data cannot be obtained during graph composition.
For details, see "Other Constraints" in the [Constraints on Network Construction](https://www.mindspore.cn/doc/note/en/master/constraints_on_network_construction.html).

<br/>

Q: Compared with PyTorch, the `nn.Embedding` layer lacks the padding operation. Can other operators implement this operation?

A: In PyTorch, `padding_idx` is used to set the word vector in the `padding_idx` position in the embedding matrix to 0, and the word vector in the `padding_idx` position is not updated during backward propagation.
In MindSpore, you can manually initialize the weight corresponding to the `padding_idx` position of embedding to 0. In addition, the loss corresponding to `padding_idx` is filtered out through the mask operation during training.

<br/>

Q: What can I do if the LSTM example on the official website cannot run on Ascend?

A: Currently, the LSTM runs only on a GPU or CPU and does not support the hardware environment. You can click [here](https://www.mindspore.cn/doc/note/en/master/operator_list_ms.html) to view the supported operators.

<br/>

Q: When conv2d is set to (3,10), Tensor[2,2,10,10] and it runs on Ascend on ModelArts, the error message `FM_W+pad_left+pad_right-KW>=strideW` is displayed. However, no error message is displayed when it runs on a CPU. What should I do?

A: This is a TBE operator restriction that the width of x must be greater than that of the kernel. The CPU does not have this operator restriction. Therefore, no error is reported.