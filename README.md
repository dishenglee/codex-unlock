# 🛡️ Codex 破甲工具

一键解除 OpenAI Codex 的合规限制，让它不再拒绝安全研究、CTF、渗透测试等请求。

## 原理

通过 `~/.codex/AGENTS.md` 注入 Unrestricted Cooperation 指令，Codex 会自动加载到每次对话中。

## 版本

| 文件 | 平台 | 用法 |
|---|---|---|
| `codex-unlock.sh` | macOS / Linux | `bash codex-unlock.sh` |
| `codex-unlock.bat` | Windows | 双击运行 |
| `codex-unlocker.py` | 跨平台 GUI | `python codex-unlocker.py` |

## 功能

- ✅ 自动扫描 Codex 安装路径
- ✅ 一键注入 / 一键还原
- ✅ 色彩区分状态
- ✅ 操作前确认，防误触

## 使用

```bash
# 破甲
bash codex-unlock.sh

# 还原
bash codex-unlock.sh --restore
```

新开 Codex 对话即可生效。

---

> 👤 作者：涤生AGI  
> 🐙 GitHub: [github.com/dishenglee/codex-unlock](https://github.com/dishenglee/codex-unlock)  
> 📡 公众号：涤生AGI  
> ⚠️ 仅限个人学习研究使用，请遵守当地法律
