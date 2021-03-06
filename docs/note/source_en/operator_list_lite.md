﻿# MindSpore Lite Operator List

`Linux` `On Device` `Inference Application` `Beginner` `Intermediate` `Expert`

<a href="https://gitee.com/mindspore/docs/blob/master/docs/note/source_en/operator_list_lite.md" target="_blank"><img src="./_static/logo_source.png"></a>

| Operation               | CPU<br/>FP16 | CPU<br/>FP32 | CPU<br/>Int8 | CPU<br/>UInt8 | GPU<br/>FP16 | GPU<br/>FP32 | Tensorflow <br/>Lite op supported | Caffe <br/>Lite op supported | Onnx <br/>Lite op supported |
|-----------------------|----------|----------|----------|-----------|----------|-------------------|----------|----------|---------|
| Abs                   | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Abs        |               | Abs                |
| Add                   | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Add        |               | Add, Int8Add                |
| AddN                  |          | Supported        |          |           |          |          | AddN       |               |                    |
| Argmax                |          | Supported        | Supported        | Supported         |          |          | Argmax     | ArgMax        | ArgMax             |
| Argmin                |          | Supported        | Supported        | Supported         |          |          | Argmin     |               |                    |
| AvgPool               | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | MeanPooling | Pooling       | AveragePool, GlobalAveragePool, Int8AveragePool        |
| BatchNorm             | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        |            | BatchNorm     | BatchNormalization |
| BatchToSpace          |          | Supported        | Supported        | Supported         | Supported         | Supported         | BatchToSpace, BatchToSpaceND |  |               |
| BiasAdd               |          | Supported        | Supported        | Supported         | Supported        | Supported         |           |                | BiasAdd            |
| Broadcast             |          | Supported        |          |           |          |          | BroadcastTo |               | Expand             |
| Cast                  | Supported        | Supported        | Supported| Supported         | Supported        | Supported        | Cast, QUANTIZE, DEQUANTIZE  |        | Cast               |
| Ceil                  | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Ceil        |               | Ceil               |
| Concat                | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Concat      | Concat        | Concat             |
| ConstantOfShape                |         | Supported        |         |          |         |         |       |         | ConstantOfShape             |
| Conv2d                | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Conv2D      | Convolution   | Conv, Int8Conv, ConvRelu, Int8ConvRelu               |
| Conv2dTranspose       | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | DeConv2D    | Deconvolution | ConvTranspose      |
| Cos                   | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Cos         |               | Cos                |
| Crop                  | Supported | Supported        | Supported        | Supported         |          |          |             |  Crop         |                    |
| DeDepthwiseConv2D     |          | Supported        | Supported        | Supported         |          |          |             |  Deconvolution| ConvTranspose      |
| DepthToSpace          |          | Supported        | Supported        | Supported         | Supported         | Supported         | DepthToSpace|               | DepthToSpace       |
| DepthwiseConv2dNative | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | DepthwiseConv2D | Convolution   |     |
| DetectionPostProcess  |          | Supported        | Supported | Supported |                   |          | Custom |           |                 |
| Div                   | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Div, RealDiv         |               | Div                |
| Eltwise               | Supported        | Supported        | Supported | Supported | Supported         | Supported         |             |  Eltwise      | Sum, Max                    |
| Elu                   |          | Supported        |          |           |          |          |        |  Elu               | Elu, NonMaxSuppression                |
| Equal                 | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | Equal       |               | Equal              |
| Exp                   |          | Supported        |          |           | Supported        | Supported        | Exp         |  Exp             | Exp                |
| ExpandDims            |          | Supported        | Supported | Supported |          |          |ExpandDims             |               |                    |
| Fill                  |          | Supported        |          |           |          |          | Fill        |               |                    |
| Flatten               |          | Supported        |          |           |          |          |             | Flatten       |                    |
| Floor                 | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | flOOR       |               | Floor              |
| FloorDiv              | Supported        | Supported        |          |           | Supported         | Supported         | FloorDiv    |               |                    |
| FloorMod              | Supported        | Supported        |          |           | Supported         | Supported         | FloorMod    |               |                    |
| FullConnection        | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | FullyConnected  | InnerProduct  |                |
| FusedBatchNorm        |          | Supported        | Supported        | Supported         |         |         | FusedBatchNorm |  |  |
| GatherNd              |          | Supported        | Supported        | Supported         |          |          | GatherND    |               |                    |
| GatherV2              |          | Supported        | Supported        | Supported         | Supported         | Supported         | Gather      |               | Gather             |
| Greater               | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | Greater     |               | Greater            |
| GreaterEqual          | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | GreaterEqual|               |                    |
| HashtableLookup       |         | Supported        |         |          |          |          | HashtableLookup   |               |                    |
| Hswish                | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | HardSwish   |               |                    |
| InstanceNorm                |         | Supported        |          |           |         |         | InstanceNorm   |               |           |
| L2Norm                |         | Supported        |          |           |         |         | L2_NORMALIZATION   |               |           |
| LayerNorm |  | Supported |  |  |  |  | LayerNorm |  |  |
| LeakyReLU             | Supported        | Supported        | Supported | Supported | Supported        | Supported        | LeakyRelu   |               | LeakyRelu          |
| Less                  | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | Less        |               | Less               |
| LessEqual             | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | LessEqual   |               |                    |
| LRN     |          | Supported        |          |           |          |          | LocalResponseNorm  |        | Lrn, LRN                |
| Log                   | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Log         |               | Log                |
| LogicalAnd            | Supported        | Supported        |          |           | Supported         | Supported         | LogicalAnd  |               | And                   |
| LogicalNot            | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | LogicalNot  |               | Not                   |
| LogicalOr             | Supported        | Supported        |          |           | Supported         | Supported         | LogicalOr   |               | Or                   |
| LshProjection         |          | Supported        |          |           |          |          | LshProjection            |               |                    |
| LSTM                  |          | Supported        |          |           |          |          |             |               | LSTM                   |
| MatMul                | Supported | Supported        | Supported        | Supported         | Supported        | Supported        |             |               | MatMul             |
| Maximum               | Supported        | Supported        |          |           | Supported         | Supported         | Maximum     |               |                |
| MaxPool               | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | MaxPooling  | Pooling       | MaxPool, GlobalMaxPool            |
| Minimum               | Supported        | Supported        |          |           | Supported         | Supported         | Minimum     |               | Min                |
| Mul                   | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Mul         |               | Mul                |
| Neg                   | Supported | Supported        |          |           | Supported         | Supported         |   Neg       |               | Neg                   |
| NotEqual              | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | NotEqual    |               |                    |
| OneHot                |          | Supported        |          |           |          |          | OneHot      |               | OneHot                   |
| Pad                   | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | Pad, MirrorPad         |               | Pad                |
| Pow                   |          | Supported        | Supported        | Supported         |          |         | Pow          | Power         | Pow              |
| PReLU                 |          | Supported        |          |           | Supported        | Supported        | PRELU       | PReLU         | PRelu             |
| Range                 |          | Supported        |          |           |          |          | Range       |               |                    |
| Rank                  |          | Supported        |          |           |          |          | Rank        |               |                    |
| ReduceASum            |          | Supported        |          |           |          |          |          |   Reduction            |           |
| ReduceMax             | Supported        | Supported        | Supported        | Supported         |          |          | ReduceMax   |               | ReduceMax          |
| ReduceMean            | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | Mean        | Reduction              | ReduceMean         |
| ReduceMin             | Supported        | Supported        | Supported        | Supported         |          |          | ReduceMin   |               | ReduceMin          |
| ReduceProd            | Supported        | Supported        | Supported        | Supported         |          |          | ReduceProd  |               | ReduceProd                   |
| ReduceSum             | Supported        | Supported        | Supported        | Supported         | Supported         | Supported         | Sum         | Reduction              | ReduceSum          |
| ReduceSumSquare       | Supported        | Supported        | Supported        | Supported         |          |          |             |  Reduction             | ReduceSumSquare                   |
| ReLU                  | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Relu        | ReLU          | Relu               |
| ReLU6                 | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Relu6       | ReLU6         | Clip*              |
| Reshape               | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Reshape     | Reshape       | Reshape,Flatten    |
| Resize                |          | Supported        | Supported        | Supported         | Supported         | Supported         | ResizeBilinear, NearestNeighbor | Interp        | Resize                   |
| Reverse               |          | Supported        |          |           |          |          | reverse     |               |                    |
| ReverseSequence       |          | Supported        |          |           |          |          | ReverseSequence  |          |                    |
| Round                 | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Round       |               | Round                   |
| Rsqrt                 | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Rsqrt       |               |                    |
| Scale                 | Supported | Supported        | Supported | Supported | Supported        | Supported        |             |  Scale        |                    |
| ScatterNd             |          | Supported        |          |           |          |          | ScatterNd   |               |                    |
| Shape                 |          | Supported        | Supported | Supported |          |          | Shape       |               | Shape              |
| Sigmoid               | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Logistic    | Sigmoid       | Sigmoid            |
| Sin                   | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Sin         |               | Sin                |
| Slice                 | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Slice       | Slice              | Slice              |
| SkipGram              |          | Supported        |         |          |         |         | SKipGram       |               |               |
| Softmax               | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Softmax     | Softmax       | Softmax            |
| SpaceToBatch          |          | Supported        | Supported        | Supported | Supported         | Supported         | SpaceToBatch |              |                    |
| SpaceToBatchND        |          | Supported        | Supported        | Supported | Supported         | Supported         | SpaceToBatchND |            |                    |
| SpaceToDepth          |          | Supported        |          |           |          |          | SpaceToDepth   |            | SpaceToDepth       |
| SparseToDense         |          | Supported        |          |           |          |          |  SpareToDense  |            |                    |
| Split                 | Supported        | Supported        | Supported        | Supported         |          |          | Split, SplitV  |            | Split                   |
| Sqrt                  | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Sqrt        |               | Sqrt               |
| Square                | Supported | Supported        | Supported        | Supported         | Supported        | Supported        | Square      |               |                    |
| SquaredDifference     | Supported | Supported        |          |           | Supported         | Supported         |  SquaredDifference |         |                    |
| Squeeze               |          | Supported        | Supported        | Supported         | Supported         | Supported         | Squeeze     |               | Squeeze            |
| StridedSlice          |          | Supported        | Supported        | Supported         |          |          | StridedSlice|               |                    |
| Stack                 | Supported | Supported        |          |           | Supported         | Supported         | Stack       |               |                    |
| Sub                   | Supported        | Supported        | Supported        | Supported         | Supported        | Supported        | Sub         |               |  Sub               |
| Swish |    | Supported |    |    |    |    | Swish | Swish | Swish |
| Tanh                  | Supported        | Supported        |          |           | Supported        | Supported        | Tanh        | TanH          | Tanh, Sign                    |
| Tile                  |          | Supported        |          |           |          |          | Tile        | Tile              | Tile               |
| TopK                  |          | Supported        | Supported        | Supported         |          |          | TopKV2      |               | TopK                   |
| Transpose             | Supported        | Supported        |          |           | Supported        | Supported        | Transpose   | Permute       | Transpose          |
| Unique                |          | Supported        |          |           |          |          | Unique      |               |                    |
| Unsqueeze             |          | Supported        | Supported        | Supported         |          |          |             |               | Unsqueeze          |
| Unstack               |          | Supported        |          |           |          |          | Unstack     |               |                    |
| Where                 |          | Supported        |          |           |          |          |  Where      |               |                    |
| ZerosLike             |          | Supported        |          |           |          |          | ZerosLike   |               |               |

* Clip: only support convert clip(0, 6) to Relu6.
