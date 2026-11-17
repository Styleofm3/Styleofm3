## 开源贡献

### DiffSynth-Studio — MiniMax-H3-Image 训练流程 Bug 修复
开源项目：DiffSynth-Studio — ⭐ 13.4K+ Stars · 1.3K+ Forks
为 DiffSynth-Studio 的 MiniMax-H3-Image 训练流水线贡献了一项 Caption 传递问题的修复。

- **问题发现：** 定位到文本特征预计算缓存中的异常，不同 Caption 被编码为完全相同的单 Token 文本特征。
- **根因分析：** 沿训练入口、参数传递及文本编码链路逐步排查，最终确认问题由 Prompt 参数传递错误引起。
- **修复验证：** 通过检查 Token 序列长度和缓存特征，验证修复后不同 Caption 能够被正确编码。
- **开源贡献：** 修复方案已被上游维护者整合，并合并至主仓库。

**相关 Pull Requests：** [#1824](https://github.com/modelscope/DiffSynth-Studio/pull/1824) · [#1828](https://github.com/modelscope/DiffSynth-Studio/pull/1828)
