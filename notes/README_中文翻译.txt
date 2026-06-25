# vLLM README 中文翻译

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/vllm-project/vllm/main/docs/assets/logos/vllm-logo-text-dark.png">
    <img alt="vLLM" src="https://raw.githubusercontent.com/vllm-project/vllm/main/docs/assets/logos/vllm-logo-text-light.png" width=55%>
  </picture>
</p>

<h3 align="center">
简单、快速、经济的 LLM 推理服务，为每个人而打造
</h3>

<p align="center">
| <a href="https://docs.vllm.ai"><b>文档</b></a> | <a href="https://blog.vllm.ai/"><b>博客</b></a> | <a href="https://arxiv.org/abs/2309.06180"><b>论文</b></a> | <a href="https://x.com/vllm_project"><b>Twitter/X</b></a> | <a href="https://discuss.vllm.ai"><b>用户论坛</b></a> | <a href="https://slack.vllm.ai"><b>开发者 Slack</b></a> |
</p>

🔥 我们已上线 vLLM 官方网站帮助你快速上手 vLLM，请访问 vllm.ai 了解更多。最新活动请访问 vllm.ai/events 加入我们。

---

## 关于 vLLM

vLLM 是一个快速且易用的 LLM 推理与服务库。

vLLM 最初由加州大学伯克利分校的 Sky Computing Lab 开发，现已成长为最活跃的开源 AI 项目之一，由来自 2000 多位贡献者、数十家学术机构和公司组成的多元化社区共同构建和维护。

### vLLM 的速度优势

- 业界领先的推理服务吞吐量
- 基于 PagedAttention 高效管理注意力机制的 Key/Value 内存
- 连续批处理（Continuous Batching）、分块预填充（Chunked Prefill）、前缀缓存（Prefix Caching）
- 通过分段式与完整 CUDA/HIP Graph 实现快速灵活的模型执行
- 量化支持：FP8、MXFP8/MXFP4、NVFP4、INT8、INT4、GPTQ/AWQ、GGUF、compressed-tensors、ModelOpt、TorchAO 以及更多
- 优化的 Attention 内核：FlashAttention、FlashInfer、TRTLLM-GEN、FlashMLA、Triton
- 优化的 GEMM/MoE 内核：使用 CUTLASS、TRTLLM-GEN、CuTeDSL 支持多种精度
- 推测解码（Speculative Decoding）：n-gram、suffix、EAGLE、DFlash
- 使用 torch.compile 实现自动内核生成与图级变换
- 分离式预填充（Prefill）、解码（Decode）和编码（Encode）

### vLLM 的灵活性与易用性

- 与热门 Hugging Face 模型无缝集成
- 高吞吐推理服务，支持多种解码算法（并行采样、束搜索等）
- 分布式推理支持张量并行（TP）、流水线并行（PP）、数据并行（DP）、专家并行（EP）和上下文并行（CP）
- 流式输出
- 使用 xgrammar 或 guidance 生成结构化输出
- 工具调用与推理解析器
- OpenAI 兼容 API 服务器，以及 Anthropic Messages API 和 gRPC 支持
- 高效的 Dense 层与 MoE 层多 LoRA 支持
- 支持 NVIDIA GPU、AMD GPU、x86/ARM/PowerPC CPU。此外还支持多种硬件插件：Google TPU、Intel Gaudi、IBM Spyre、华为昇腾、Rebellions NPU、Apple Silicon、MetaX GPU 等

### 模型支持

vLLM 无缝支持 200+ 种 HuggingFace 模型架构，包括：

- Decoder-only 类 LLM（如 Llama、Qwen、Gemma）
- 混合专家型 LLM（Mixture-of-Expert，如 Mixtral、DeepSeek-V3、Qwen-MoE、GPT-OSS）
- 混合注意力与状态空间模型（如 Mamba、Qwen3.5）
- 多模态模型（如 LLaVA、Qwen-VL、Pixtral）
- 嵌入与检索模型（如 E5-Mistral、GTE、ColBERT）
- 奖励与分类模型（如 Qwen-Math）

完整支持模型列表见 vLLM 文档。

## 快速开始

使用 uv（推荐）或 pip 安装 vLLM：

```bash
uv pip install vllm
```

或从源码构建用于开发。

访问 vLLM 文档了解更多：

- 安装指南
- 快速入门
- 支持的模型列表

## 贡献

我们欢迎并珍视任何形式的贡献与合作。请参阅"向 vLLM 贡献"文档了解如何参与。

## 引用

如果你在研究中使用了 vLLM，请引用我们的论文：

@inproceedings{kwon2023efficient,
  title={Efficient Memory Management for Large Language Model Serving with PagedAttention},
  author={Woosuk Kwon and Zhuohan Li and Siyuan Zhuang and Ying Sheng and Lianmin Zheng and Cody Hao Yu and Joseph E. Gonzalez and Hao Zhang and Ion Stoica},
  booktitle={Proceedings of the ACM SIGOPS 29th Symposium on Operating Systems Principles},
  year={2023}
}

## 联系我们

- 技术问题与功能请求：请使用 GitHub Issues
- 与其他用户讨论：请使用 vLLM 论坛
- 贡献与开发协调：请使用 Slack
- 安全漏洞报告：请使用 GitHub 的安全通告功能
- 合作与伙伴关系：请联系 collaboration@vllm.ai

## 媒体资源

- 如需使用 vLLM Logo，请参阅媒体资源仓库