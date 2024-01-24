## Source
https://arxiv.org/pdf/2109.05418.pdf  
https://github.com/bytedance/music_source_separation  
https://huggingface.co/spaces/akhaliq/Music_Source_Separation  

## Problem(What)
Former MSS: 通常用于学习从混合声谱（spectrogram）--> 一组声谱，声谱图只有幅度，有一下限制

- 性能障碍（不正确的相位重构导致）
- 掩码限制（0-1 外还有 22% 超过1）
- 深架构潜力被忽略

## Solution(How)

架构 143层 resUnet
- 6 REB 6RDB 均含有 4x RCB， 后者有上采样的transposed转置卷积层
- RCB 有2个卷积层 3x3 卷积核 输入输出有快捷连结 leaky ReLU（0.01负斜率）2x2 池化层减小特征图大小
- REB和RDB之间有中间卷积块4xICB 含4xRCB


## Contributions（Where）
 - 通过cIRM来估计相位，解耦幅度和相位
 - 扩展分离方法允许掩码幅度大于1
 - 提出143层的残差UNet架构，在人声、贝斯、其它和伴奏方便表现优秀


## Inspiration(Matters)
- [ ] UNet
- [ ] ResNet
- [ ] ResUnet

## Related Concepts

MSS（Music Souce Separation）: 音乐源分离

MIR（Music Information Retrieval）: 音乐信息检索

SDR（signal-to-distortion ration）: 信噪比

CSMT: 中国声音与音乐技术会议

MUDB18数据集：










