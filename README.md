# UI5 MCP Server

## 项目说明

本项目是基于 [UI5/mcp-server](https://github.com/UI5/mcp-server) 的分支版本，旨在为 SAP UI5/OpenUI5 应用开发提供 MCP (Model Context Protocol) 支持。

原始项目地址：[https://github.com/UI5/mcp-server](https://github.com/UI5/mcp-server)

## 其它SAP中AI的开发使用
其它SAP中AI的开发使用可参考[AI的ABAP开发中的使用](https://www.ut163.com/the_use_of_ai_in_abap_development/)


## 功能特性

- **创建 UI5 应用**：快速生成新的 UI5 项目
- **API 参考文档**：获取 UI5 API 文档和示例
- **开发规范指南**：提供 UI5 开发的最佳实践
- **Manifest 验证**：验证 UI5 应用的 manifest.json 配置
- **代码检查**：集成 UI5 Linter 进行代码分析和问题检测
- **项目信息获取**：提取 UI5 项目的元数据和配置信息
- **TypeScript 转换指南**：提供 JavaScript 到 TypeScript 的转换指导

## 可用工具

| 工具名称 | 功能描述 |
|---------|---------|
| `create_ui5_app` | 基于模板创建新的 UI5 应用 |
| `create_integration_card` | 创建 UI Integration Card |
| `get_api_reference` | 获取 UI5 API 文档 |
| `get_guidelines` | 获取 UI5 开发规范 |
| `get_project_info` | 获取项目信息 |
| `run_ui5_linter` | 运行 UI5 Linter 检查代码 |
| `run_manifest_validation` | 验证 manifest 配置 |
| `get_version_info` | 获取 UI5 版本信息 |

## 系统要求

- **Node.js**：v20.17.0、v22.9.0 或更高版本
- **npm**：v8.0.0 或更高版本
- **MCP 客户端**：如 TRAE IDE、VS Code (GitHub Copilot)、Cline 等

## 安装步骤

### 第一步：从 GitHub 下载项目

访问原始项目地址下载：

**原始项目（推荐）：**
```
https://github.com/UI5/mcp-server
```

**本分支版本：**
```
https://github.com/yan252/mcp-ui5-server
```

下载方式：
1. 使用 Git 克隆：
   ```bash
   git clone https://github.com/yan252/mcp-ui5-server
   ```
2. 或直接下载 ZIP 压缩包

### 第二步：安装依赖

进入项目目录并安装依赖：

```bash
cd mcp-ui5-server
npm install
```

### 第三步：构建项目

```bash
npm run build
```

## 在 TRAE IDE 中配置 MCP

### 打开 TRAE MCP 配置

1. 打开 TRAE IDE 设置
2. 找到 **MCP Server** 配置选项
3. 选择 **INSERT** → **BINDING** 或编辑配置文件

### 配置示例

下面是我的TRAE中配置配置文件，其它用户请根据实际目录修改其中的目录地址，确保路径正确，其它AI软件的使用配置可参考此及源项目配置：

```json
{
  "mcpServers": {
    "ui5-mcp-server": {
      "command": "C:\\Users\\96000217\\node-v22.11.0\\node-v22.11.0-win-x64\\node.exe",
      "args": [
        "C:\\Users\\96000217\\Documents\\trae_projects\\mcp-ui5-server\\bin\\ui5mcp.js"
      ]
    }
  }
}
```

### 配置说明

- **`command`**：Node.js 可执行文件路径
  - 示例：`C:\Users\96000217\node-v22.11.0\node-v22.11.0-win-x64\node.exe`
  - 请根据您实际的 Node.js 安装路径进行调整，也可以通过命令行查看：`where node`，或者在此直接使用 `node.exe`

- **`args`**：MCP 服务器入口文件路径
  - 示例：`C:\Users\96000217\Documents\trae_projects\mcp-ui5-server\bin\ui5mcp.js`
  - 请根据您实际的项目存放路径进行调整

### 路径调整指南

如果您修改了项目存放位置，需要相应调整配置：

1. **Node.js 路径**：找到您系统上 Node.js 的安装位置
   - Windows 上可通过命令行查看：`where node`

2. **ui5mcp.js 路径**：指向本项目 bin 目录下的 ui5mcp.js 文件

## 快速验证

配置完成后，可以在 TRAE 中测试 MCP 服务器是否正常工作：

1. 重启 TRAE IDE
2. 尝试询问 MCP 服务器可用工具列表
3. 尝试创建一个新的 UI5 应用

## 使用示例

### 创建 UI5 应用

```
appNamespace: com.myorg.myapp
basePath: C:\Projects\my-app
oDataV4Url: http://localhost:4004/odata/v4/service
oDataEntitySet: Orders
typescript: true
```

### 获取 UI5 指南

```
使用 get_guidelines 工具获取最新的 UI5 开发规范和最佳实践
```

## 技术支持

- **原始项目**：[UI5/mcp-server Issues](https://github.com/UI5/mcp-server/issues)
- **本项目 Issues**：[yan252/mcp-ui5-server Issues](https://github.com/yan252/mcp-ui5-server/issues)
- **社区讨论**：[SAP Community](https://community.sap.com/)
- **其他资源**：[AI的ABAP开发中的使用](https://www.ut163.com/the_use_of_ai_in_abap_development/)
- **其他资源**：[我的SAP学习网站](https://www.ut163.com/)





## 许可证

本项目遵循 Apache-2.0 许可证。详细许可证信息请参阅 [LICENSE](./LICENSE) 文件。

## 致谢

感谢 [SAP](https://www.sap.com) 和所有 [UI5/mcp-server](https://github.com/UI5/mcp-server) 的贡献者。
