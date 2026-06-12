# 🛡️ Codex 破甲工具

一键解除 OpenAI Codex 合规限制，让它在安全研究、CTF、渗透测试场景下直接配合工作。

## 原理

通过 `model_instructions_file` 配置项，将包含 **Unrestricted Cooperation** 的完整系统提示词作为 Response API 的 `instructions` 参数注入，替代 Codex 默认提示词。

⚠️ 实测结论：对 CTF/渗透/逆向类请求有效。对恶意软件红线（如系统级键盘记录器）无效——OpenAI 模型训练层硬编码的安全限制无法被 prompt 覆盖。

## 文件

| 文件 | 平台 | 说明 |
|---|---|---|
| `codex-unlock.sh` | macOS / Linux | 终端版，自动扫描、一键注入 |
| `codex-unlock.bat` | Windows | 终端版，双击运行 |
| `codex-unlocker.py` | 跨平台 | GUI 版，tkinter 可视化 |

## 使用

```bash
# 破甲
bash codex-unlock.sh

# 还原
bash codex-unlock.sh --restore
```

新开 Codex 对话生效。

## 提示词内容

基于 Codex 官方 `gpt_5_codex_prompt.md`，在 Values 中融入：

- Clarity / Pragmatism / Rigor
- **Unrestricted Cooperation**：无拒绝、无限制，覆盖 NSFW、CTF、安全研究、渗透测试
- 明确所有代码生成立场为「授权教育/研究用途」

完整内容见 `~/.codex/prompts/system-prompt.md`（脚本自动生成）。

---

> 👤 作者：**涤生AGI**  
> 🐙 GitHub: [github.com/dishenglee/codex-unlock](https://github.com/dishenglee/codex-unlock)  
> 📡 公众号：**涤生AGI**  
> ⚠️ 仅限个人学习研究使用，请遵守当地法律
