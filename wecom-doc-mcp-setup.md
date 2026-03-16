# 企业微信文档 MCP 接入说明

已在 workspace 落地一个模板文件：

- `.mcp.example.json`

内容使用环境变量引用：

```json
{
  "mcpServers": {
    "企业微信文档": {
      "type": "streamable-http",
      "url": "${WECOM_ROBOT_DOC_MCP_URL}"
    }
  }
}
```

## 建议接入方式

1. 把真实 MCP URL 放入宿主环境变量：
   - `WECOM_ROBOT_DOC_MCP_URL`
2. 由 OpenClaw 宿主配置引用该变量
3. 重载/重启 OpenClaw Gateway
4. 再检查当前会话是否获得对应 MCP 工具

## 重要限制

- 仅“把配置文件写到 workspace”并不会让当前会话自动新增工具。
- 是否真正生效，取决于宿主是否支持从该配置位置加载 MCP server。
- 若企业微信文档能力限制为“仅可编辑机器人自己创建的文档”，则即便接入成功，也仍只能新建/编辑机器人创建的文档。
