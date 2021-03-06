# HRNet系列

## 概述
HRNet是2019年由微软亚洲研究院提出的一种全新的神经网络，不同于以往的卷积神经网络，该网络在网络深层仍然可以保持高分辨率，因此预测的关键点热图更准确，在空间上也更精确。此外，该网络在对分辨率敏感的其他视觉任务中，如检测、分割等，表现尤为优异。

该系列模型的FLOPS、参数量以及FP32预测耗时如下图所示。

![](../../images/models/HRNet.png.flops.png)

![](../../images/models/HRNet.png.params.png)

![](../../images/models/HRNet.png.fp32.png)
目前PaddleClas开源的这类模型的预训练模型一共有7个，其指标如图所示，其中HRNet_W48_C指标精度异常的原因可能是因为网络训练的正常波动。


## 精度、FLOPS和参数量

| Models      | Top1   | Top5   | Reference<br>top1 | Reference<br>top5 | FLOPS<br>(G) | Parameters<br>(M) |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| HRNet_W18_C | 0.769  | 0.934  | 0.768             | 0.934             | 4.140        | 21.290            |
| HRNet_W30_C | 0.780  | 0.940  | 0.782             | 0.942             | 16.230       | 37.710            |
| HRNet_W32_C | 0.783  | 0.942  | 0.785             | 0.942             | 17.860       | 41.230            |
| HRNet_W40_C | 0.788  | 0.945  | 0.789             | 0.945             | 25.410       | 57.550            |
| HRNet_W44_C | 0.790  | 0.945  | 0.789             | 0.944             | 29.790       | 67.060            |
| HRNet_W48_C | 0.790  | 0.944  | 0.793             | 0.945             | 34.580       | 77.470            |
| HRNet_W64_C | 0.793  | 0.946  | 0.795             | 0.946             | 57.830       | 128.060           |


## FP32预测速度

| Models      | Crop Size | Resize Short Size | Batch Size=1<br>(ms) |
|-------------|-----------|-------------------|--------------------------|
| HRNet_W18_C | 224       | 256               | 7.368                    |
| HRNet_W30_C | 224       | 256               | 9.402                    |
| HRNet_W32_C | 224       | 256               | 9.467                    |
| HRNet_W40_C | 224       | 256               | 10.739                   |
| HRNet_W44_C | 224       | 256               | 11.497                   |
| HRNet_W48_C | 224       | 256               | 12.165                   |
| HRNet_W64_C | 224       | 256               | 15.003                   |
