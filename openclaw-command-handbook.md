# OpenClaw 常用操作命令完整速查手册

> 从入门到精通的终端 CLI & 聊天指令全解析 🔥

---

## 导语：为什么你需要这份命令手册？

OpenClaw 是一个强大的 AI 助手平台，支持多种消息渠道（微信、飞书、钉钉、Telegram 等）和丰富的功能扩展。掌握这些命令，可以让你：

- ✅ 快速诊断和解决问题
- ✅ 高效管理多模型、多通道
- ✅ 自动化日常任务
- ✅ 扩展 AI 能力（技能、插件）

---

## 命令分类总览

| 类别 | 说明 | 使用频率 |
|------|------|----------|
| 基础操作 | 状态查看、帮助信息 | ⭐⭐⭐ |
| 网关管理 | Gateway 核心引擎控制 | ⭐⭐⭐ |
| 通道管理 | 微信/飞书/钉钉等对接 | ⭐⭐ |
| 模型管理 | 多模型切换和配置 | ⭐⭐⭐ |
| 插件技能 | 功能扩展管理 | ⭐⭐ |
| 聊天命令 | 会话控制、历史管理 | ⭐⭐⭐ |

---

## 第一部分：🖥️ 终端 CLI 命令详解

### 一、基础操作（每日必用 ⭐⭐⭐）

```bash
# 查看 OpenClaw 版本
openclaw --version

# 查看帮助信息
openclaw --help
openclaw <command> --help

# 查看系统状态
openclaw status

# 打开 Web Dashboard
openclaw dashboard
```

### 二、诊断与排错（出问题先跑这个 ⭐⭐⭐）

```bash
# 全面诊断
openclaw doctor

# 检查配置
openclaw config list

# 查看日志
openclaw logs

# 测试消息通道
openclaw message test
```

### 三、网关 Gateway 管理（核心引擎）

```bash
# 查看网关状态
openclaw gateway status

# 启动网关
openclaw gateway start

# 停止网关
openclaw gateway stop

# 重启网关
openclaw gateway restart

# 查看网关日志
openclaw gateway logs
```

### 四、模型管理（多模型切换核心）

```bash
# 列出可用模型
openclaw models list

# 设置默认模型
openclaw models default <model-name>

# 查看当前模型
openclaw models current

# 测试模型
openclaw models test
```

**常用模型别名：**
- `gpt-4` / `gpt-4o` - OpenAI GPT-4
- `claude` - Anthropic Claude
- `kimi` - 月之暗面 Kimi
- `glm` - 智谱 GLM
- `deepseek` - DeepSeek

### 五、聊天通道 Channel 管理（对接微信/飞书/钉钉）

```bash
# 列出已配置的通道
openclaw channel list

# 查看通道状态
openclaw channel status

# 测试通道连接
openclaw channel test <channel-name>

# 启用/禁用通道
openclaw channel enable <channel-name>
openclaw channel disable <channel-name>
```

**支持的通道：**
- `wechat` - 微信
- `feishu` - 飞书
- `dingtalk` - 钉钉
- `telegram` - Telegram
- `discord` - Discord
- `slack` - Slack
- `whatsapp` - WhatsApp

### 六、定时任务 Cron 管理

```bash
# 列出所有定时任务
openclaw cron list

# 添加定时任务
openclaw cron add --name "任务名" --cron "0 9 * * *" --message "提醒内容"

# 删除定时任务
openclaw cron delete <job-id>

# 查看任务详情
openclaw cron show <job-id>
```

### 七、技能 Skill 管理（AI 能力扩展）

```bash
# 列出已安装技能
openclaw skills list

# 检查技能状态
openclaw skills check

# 查看技能详情
openclaw skills info <skill-name>
```

**常用技能：**
- `github` - GitHub 操作
- `weather` - 天气查询
- `notion` - Notion 集成
- `obsidian` - Obsidian 笔记
- `summarize` - 内容总结
- `tavily` - AI 搜索

### 八、浏览器控制（自动化操作）

```bash
# 查看浏览器状态
openclaw browser status

# 启动浏览器
openclaw browser start

# 停止浏览器
openclaw browser stop
```

---

## 第二部分：💬 聊天斜杠命令详解

### 一、会话管理（最常用 ⭐⭐⭐）

| 命令 | 说明 |
|------|------|
| `/reset` | 重置当前会话（清空上下文） |
| `/clear` | 清屏 |
| `/status` | 查看当前会话状态 |
| `/model <name>` | 切换模型 |
| `/models` | 列出可用模型 |

### 二、模型切换（多模型对比测试）

```
/model gpt-4      # 切换到 GPT-4
/model claude     # 切换到 Claude
/model kimi       # 切换到 Kimi
```

### 三、会话历史管理

| 命令 | 说明 |
|------|------|
| `/history` | 查看会话历史 |
| `/history --export` | 导出历史记录 |
| `/history --clear` | 清空历史 |

### 四、工具与执行控制

| 命令 | 说明 |
|------|------|
| `/tools` | 列出可用工具 |
| `/tool <name>` | 使用指定工具 |
| `/exec <command>` | 执行 shell 命令 |

### 五、信息查询

| 命令 | 说明 |
|------|------|
| `/help` | 显示帮助 |
| `/about` | 关于 OpenClaw |
| `/version` | 版本信息 |

---

## 第三部分：📁 关键文件路径速查表

| 路径 | 说明 |
|------|------|
| `~/.openclaw/` | OpenClaw 配置目录 |
| `~/.openclaw/config.yaml` | 主配置文件 |
| `~/.openclaw/extensions/` | 插件目录 |
| `~/.openclaw/workspace/` | 工作区目录 |
| `~/.openclaw/logs/` | 日志目录 |

---

## 第四部分：🆘 新手急救流程

### 遇到问题按这个来：

1. **先检查状态**
   ```bash
   openclaw status
   openclaw doctor
   ```

2. **查看日志**
   ```bash
   openclaw logs
   ```

3. **重启网关**
   ```bash
   openclaw gateway restart
   ```

4. **检查配置**
   ```bash
   openclaw config list
   ```

5. **测试通道**
   ```bash
   openclaw channel test
   ```

---

## 第五部分：🎯 必备命令速记

### 🔥 高频命令（每天使用）

```bash
openclaw status          # 查看状态
openclaw dashboard       # 打开网页控制台
openclaw gateway restart # 重启网关
/model <name>            # 切换模型
/reset                   # 重置会话
```

### 🛠️ 故障排查速记

```bash
openclaw doctor          # 全面诊断
openclaw logs            # 查看日志
openclaw gateway logs    # 网关日志
```

### 📱 通道管理速记

```bash
openclaw channel list    # 列出通道
openclaw channel test    # 测试通道
```

### 🤖 模型管理速记

```bash
openclaw models list     # 列出模型
openclaw models default  # 设置默认
/model <name>            # 快速切换
```

### 🔌 插件技能速记

```bash
openclaw skills list     # 列出技能
openclaw skills check    # 检查状态
```

---

## 结语：成为 OpenClaw 高手的下一步

1. **多练习** - 每天使用这些命令
2. **看日志** - 遇到问题先看日志
3. **读文档** - https://docs.openclaw.ai
4. **加社区** - 参与 OpenClaw 社区讨论

---

## 参考链接

- OpenClaw 官方文档：https://docs.openclaw.ai
- GitHub 仓库：https://github.com/openclaw/openclaw
- ClawHub 技能商店：https://clawhub.com

---

*本文档基于 OpenClaw 2026.2.23 版本整理*
*最后更新：2025-02-27*
