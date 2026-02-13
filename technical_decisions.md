## 2026.2.14 技术决策记录

- **问题**：Hugging Face 国内无法访问 + 4-bit 量化兼容性问题
- **方案**：
  1. 切换至魔搭（ModelScope）加载 Qwen 模型
  2. 改用 `torch.float16` 替代 `load_in_4bit`
- **结果**：
  - 成功在 RTX 4090D 24G 上运行 Qwen-1.5-1.8B
  - 显存占用 ~10GB，生成质量良好
- **验证**：见 `output.txt`
