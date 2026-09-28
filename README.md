# 🤖 企业级 RAG + Agent 智能问答系统

基于 **LangChain**、**大模型 API** 与 **Streamlit** 打造的拥有工具调用能力（Tool Calling）和检索增强生成（RAG）的 AI 智能体（Agent）系统。

---

## 🌟 核心功能特性

- 🧠 **ReAct 智能体架构**：基于 `Thought -> Action -> Observation` 的思考链路，大模型具备自主规划与决策能力。
- 🛠️ **Tool Calling 外部工具集成**：支持自定义 `@tool` 装饰器，使 AI 长出“手脚”，能够自动调用外部 API（如查询实时数据、订单查询、计算器等）。
- 📚 **高级 RAG 检索增强**：结合本地知识库（向量数据库），在 AI 执行任务时提供精准的私有领域知识支撑，彻底消除幻觉。
- 💬 **流式交互 Web 界面**：基于 Streamlit 构建的前后端分离/容器化架构，支持带有 `Session State` 的多轮上下文记忆流式对话。
- ⚙️ **灵活的配置管理**：解耦式目录架构设计，轻松抽离与替换底层 LLM（如 OpenAI、DeepSeek 等）及 Embedding 模型。

---

## 📁 核心目录结构

```text
├── agent/            # Agent 智能体核心逻辑与路由控制
├── rag/              # 知识库构建与 Retriever 检索链
├── tools/            # 供大模型调用的 Custom Tools 集合
├── utils/            # 日志、格式化等通用辅助函数
├── app.py            # Streamlit 交互式 Web 主程序
└── requirements.txt  # 项目依赖清单

🚀 快速启动指南
1. 克隆本项目
code
Bash
git clone https://github.com/2905328457a-lgtm/LLM-Agent-RAG-System.git
cd LLM-Agent-RAG-System
2. 安装依赖环境
推荐使用 Python 3.10+ 版本：
code
Bash
pip install -r requirements.txt
3. 配置环境变量
在项目根目录下新建 .env 文件，填入所需的大模型 API Key：
code
Text
DEEPSEEK_API_KEY="sk-你的DeepSeek密钥"
# 其他自定义配置...
4. 启动应用
code
Bash
streamlit run app.py
启动后，浏览器将自动打开 http://localhost:8501。
