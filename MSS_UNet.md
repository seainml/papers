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









