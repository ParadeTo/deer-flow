# 🦌 DeerFlow 分阶段学习指南

本指南为每个学习阶段创建了对应的git分支，你可以按顺序切换到不同分支学习项目的演进过程。

## 📋 学习分支总览

```bash
# 查看所有学习分支
git branch | grep learning

# 切换到指定学习分支
git checkout learning/01-core-foundation
```

## 🎯 详细学习路径

### 第一阶段：核心基础 `learning/01-core-foundation`
**基于commit:** `03798de` (2025年4月7日)
**学习重点:** 理解项目最初的架构和核心概念

```bash
git checkout learning/01-core-foundation
```

**核心文件学习:**
- `src/graph/nodes.py` - 多智能体节点实现
- `src/workflow.py` - 基础工作流程
- `src/prompts/planner.md` - 规划智能体提示词
- `src/prompts/researcher.md` - 研究智能体提示词
- `src/prompts/reporter.md` - 报告生成提示词
- `main.py` - 命令行入口

**学习任务:**
1. 运行 `uv run main.py "什么是人工智能？"` 体验基础功能
2. 理解多智能体协作机制
3. 分析各个提示词的设计思路
4. 学习LangGraph的基本使用

---

### 第二阶段：搜索引擎扩展 `learning/02-search-engines`
**基于commit:** `3a342a6` (2025年4月初)
**学习重点:** 多搜索引擎集成和内容抓取

```bash
git checkout learning/02-search-engines
```

**新增功能:**
- DuckDuckGo搜索引擎支持
- Arxiv学术搜索
- Brave搜索引擎
- Tavily搜索优化

**核心文件:**
- `src/tools/search.py` - 搜索工具封装
- `src/tools/crawl.py` - 网页内容抓取
- `src/crawler/` - 爬虫相关模块

**学习任务:**
1. 配置不同的搜索引擎API
2. 测试各种搜索引擎的效果差异
3. 理解搜索结果的处理流程

---

### 第三阶段：服务器架构 `learning/03-server-architecture`
**基于commit:** `510ba73` (2025年4月13日)
**学习重点:** Web服务和API设计

```bash
git checkout learning/03-server-architecture
```

**新增功能:**
- FastAPI Web服务器
- RESTful API接口
- SSE流式响应
- 基础的聊天API

**核心文件:**
- `server.py` - 服务器启动脚本
- `src/server/app.py` - FastAPI应用主体
- `src/server/chat_request.py` - 请求处理逻辑

**学习任务:**
1. 启动服务器: `python server.py`
2. 测试API接口: `curl http://localhost:8000/api/chat`
3. 理解流式响应的实现
4. 学习FastAPI的基本用法

---

### 第四阶段：人机交互优化 `learning/04-human-interaction`
**基于commit:** `a7ae47f` (2025年4月中)
**学习重点:** Human-in-the-loop机制

```bash
git checkout learning/04-human-interaction
```

**新增功能:**
- 人工干预机制
- 计划审核和修改
- 中断协议支持
- 交互式计划调整

**学习任务:**
1. 体验人工审核研究计划的流程
2. 理解中断和恢复机制
3. 学习如何设计用户友好的交互

---

### 第五阶段：Web UI集成 `learning/05-web-ui-integration`
**基于commit:** `fd7a803` (2025年4月17日)
**学习重点:** 现代Web前端开发

```bash
git checkout learning/05-web-ui-integration
```

**新增功能:**
- Next.js 14+ React应用
- TypeScript类型系统
- Tailwind CSS样式
- 实时消息流显示
- 研究过程可视化

**核心目录:**
- `web/src/app/` - Next.js应用结构
- `web/src/components/` - React组件
- `web/src/core/` - 核心业务逻辑

**学习任务:**
1. 安装前端依赖: `cd web && pnpm install`
2. 启动开发服务器: `./bootstrap.sh -d`
3. 访问 http://localhost:3000
4. 学习React Hooks和现代前端开发

---

### 第六阶段：内容创作功能 `learning/06-content-creation`
**基于commit:** `a6ab97c` (2025年夏季)
**学习重点:** 多媒体内容生成

```bash
git checkout learning/06-content-creation
```

**新增功能:**
- Volcengine TTS语音合成
- Podcast音频生成
- PPT演示文稿创建
- 音频参数调节

**学习任务:**
1. 配置TTS API密钥
2. 测试语音合成功能
3. 生成podcast音频
4. 理解多媒体内容生成流程

---

### 第七阶段：RAG知识库集成 `learning/07-rag-integration`
**基于commit:** `462752b` (2025年秋季)
**学习重点:** 私有知识库和检索增强生成

```bash
git checkout learning/07-rag-integration
```

**新增功能:**
- RAGFlow集成
- 私有文档检索
- 向量数据库支持
- 知识库管理

**核心文件:**
- `src/rag/` - RAG相关模块
- `src/tools/retriever.py` - 检索工具

**学习任务:**
1. 配置RAGFlow服务
2. 上传测试文档
3. 测试私有知识库检索
4. 理解RAG的工作原理

---

### 第八阶段：MCP协议扩展 `learning/08-mcp-protocol`
**基于commit:** `75ad3e0` (2025年冬季)
**学习重点:** Model Context Protocol集成

```bash
git checkout learning/08-mcp-protocol
```

**新增功能:**
- MCP服务器支持
- 外部工具集成
- 协议标准化
- 可扩展插件架构

**学习任务:**
1. 理解MCP协议标准
2. 配置MCP服务器
3. 集成外部工具和服务
4. 开发自定义MCP插件

---

### 第九阶段：深度思考功能 `learning/09-deep-think`
**基于commit:** `19fa1e9` (2025年末)
**学习重点:** AI推理过程可视化

```bash
git checkout learning/09-deep-think
```

**新增功能:**
- Deep Think推理模式
- 思考过程可视化
- 推理链展示
- 高级AI能力

**学习任务:**
1. 启用深度思考模式
2. 观察AI的推理过程
3. 理解思维链技术
4. 优化推理质量

---

### 第十阶段：国际化支持 `learning/10-i18n-support`
**基于commit:** `e1187d7` (2025年末)
**学习重点:** 多语言和本地化

```bash
git checkout learning/10-i18n-support
```

**新增功能:**
- 多语言界面支持
- 本地化配置
- 国际化最佳实践
- 多语言内容生成

**核心文件:**
- `web/messages/` - 多语言配置
- `web/src/i18n.ts` - 国际化配置

**学习任务:**
1. 切换不同语言界面
2. 添加新的语言支持
3. 理解i18n最佳实践
4. 测试多语言内容生成

---

## 🚀 快速开始

```bash
# 1. 从第一阶段开始
git checkout learning/01-core-foundation

# 2. 安装依赖
uv sync

# 3. 配置环境
cp conf.yaml.example conf.yaml
cp .env.example .env

# 4. 运行项目
uv run main.py "你好，DeerFlow！"

# 5. 学习完当前阶段后，切换到下一阶段
git checkout learning/02-search-engines
```

## 💡 学习建议

1. **按顺序学习:** 每个分支都建立在前一个的基础上
2. **动手实践:** 不要只看代码，要实际运行和测试
3. **对比差异:** 使用 `git diff` 查看各阶段间的变化
4. **记录笔记:** 为每个阶段记录学习心得
5. **实验修改:** 在理解基础上尝试小的修改和改进

## 🔍 查看分支差异

```bash
# 查看两个学习阶段之间的差异
git diff learning/01-core-foundation learning/02-search-engines

# 查看特定文件的变化
git diff learning/01-core-foundation learning/02-search-engines -- src/tools/search.py
```

## 📚 进阶学习

完成所有学习分支后，你可以：

1. **回到主分支:** `git checkout main` 体验最新完整功能
2. **创建实验分支:** 基于学习分支创建自己的功能分支
3. **贡献代码:** 理解项目后可以提交PR贡献代码
4. **自定义扩展:** 基于学到的架构开发自己的功能

---

祝你学习愉快！🎉
