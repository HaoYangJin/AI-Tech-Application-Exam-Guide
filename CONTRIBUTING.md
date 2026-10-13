# 纠错与维护指引

感谢帮助核对这份学习资料。可通过 [Issue](https://github.com/HaoYangJin/AI-Tech-Application-Exam-Guide/issues/new?template=correction.md) 反馈，也可提交针对仓库文档的 Pull Request。

## 提交纠错

请尽量提供：

- PDF 版本或 SHA-256、物理页码及知识点编号，例如「第 22 页，3.1.6 性能评估」。
- 出现问题的短原文、公式、代码行或排版位置。
- 建议修改和理由；涉及知识表述时附教材章节、官方文档或论文来源。
- 涉及运行错误时附 Python 与相关库版本、最小复现步骤和报错文本。

不要在 Issue 中公开个人信息、访问令牌或整章受版权保护的教材扫描件。讨论以概念、计算和来源为依据；与 2025 年版考纲不同的新考纲内容请明确标明版本。

## 修改文档

保持「知识领域 → 知识单元 → 知识点」层级及考核要求与考纲对应。基础与综合模块中的同名知识点承担不同深度，不应直接去重。

引用原文与补充讲解需要分开标注。修订原文选段时同步核对来源，不把独立概括冒称原作者原话。第三方材料的使用条件见 [THIRD_PARTY_NOTICES](./THIRD_PARTY_NOTICES.md)。

本仓库当前不含完整排版源稿或自动构建脚本。PDF 内容纠错可先通过 Issue 明确修改，再由维护者重新排版发布。

## 更新 PDF 后的核对

1. 保留根目录现有 PDF 文件名，检查文件可打开、文字清晰且书签可用。
2. 按实际文档更新 README 的页数、覆盖统计及 [知识点导航](./docs/OUTLINE.md)。
3. 新增或更换来源时同步修改 [参考资料索引](./docs/SOURCES.md) 和正文来源编号。
4. 重新计算 SHA-256，更新 `SHA256SUMS` 并记录到 [CHANGELOG](./CHANGELOG.md)。
5. 检查 Markdown 相对链接、PDF 页码目标与源内容对应；代码验证只描述实际完成的检查。

可在 Windows PowerShell 中核对文件摘要：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\人工智能技术及应用_二三级考纲知识点详解.pdf'
```

将输出与 `SHA256SUMS` 比较。摘要一致说明文件字节一致，不代表内容不存在知识错误。
