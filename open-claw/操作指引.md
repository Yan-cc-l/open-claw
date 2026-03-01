# OpenClaw 操作指引

本文档整理了 OpenClaw 常用的 CLI 命令及其用途。

## 服务管理

| 命令 | 说明 |
|------|------|
| `openclaw gateway status` | 查看 Gateway 服务状态 |
| `openclaw gateway start` | 启动 Gateway 服务 |
| `openclaw gateway stop` | 停止 Gateway 服务 |
| `openclaw gateway restart` | 重启 OpenClaw 服务 |

## 系统状态

| 命令 | 说明 |
|------|------|
| `openclaw status` | 查看 OpenClaw 整体状态 |
| `openclaw version` | 查看当前版本 |
| `openclaw doctor` | 诊断系统问题 |

## 配置管理

| 命令 | 说明 |
|------|------|
| `openclaw config get <key>` | 获取配置项 |
| `openclaw config set <key> <value>` | 设置配置项 |
| `openclaw config list` | 列出所有配置 |

## 会话管理

| 命令 | 说明 |
|------|------|
| `openclaw sessions list` | 列出所有会话 |
| `openclaw sessions logs <session-id>` | 查看会话日志 |

## 技能管理 (Skills)

| 命令 | 说明 |
|------|------|
| `openclaw skills list` | 列出已安装的技能 |
| `openclaw skills install <skill-name>` | 安装技能 |
| `openclaw skills uninstall <skill-name>` | 卸载技能 |
| `openclaw skills update <skill-name>` | 更新技能 |

## 节点管理 (Nodes)

| 命令 | 说明 |
|------|------|
| `openclaw nodes list` | 列出已配对的节点 |
| `openclaw nodes status` | 查看节点状态 |

## 帮助

| 命令 | 说明 |
|------|------|
| `openclaw help` | 显示帮助信息 |
| `openclaw <command> --help` | 查看具体命令的帮助 |

---

*文档创建时间：2026-02-26*
*仓库：https://github.com/Yan-cc-l/open-claw*
