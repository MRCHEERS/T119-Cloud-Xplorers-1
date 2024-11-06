# T119-Cloud-Xplorers: Cathay Travel AI

基于 FastGPT+ 和 Docker 构建的智能旅行助手系统，为国泰航空提供智能化服务支持。

## 项目概述

本项目是一个基于大语言模型的智能旅行助手系统，通过整合 ChatGLM 和 Azure 服务，为用户提供智能化的旅行相关服务。

### 核心特性

- 🤖 基于 ChatGLM 的智能对话系统
- 🔄 FastGPT+ 提供的流程编排能力
- 🐳 Docker 容器化部署支持
- ☁️ Azure 云服务集成
- 🛫 专业的航空旅行知识库

## 技术栈

- **基础框架**: FastGPT+
- **容器化**: Docker
- **大语言模型**: 
  - ChatGLM (微调模型)
  - Azure OpenAI Service
- **部署环境**: Docker Compose

## 快速开始

### 环境要求

- Docker 20.10.0+
- Docker Compose v2.0.0+
- Node.js 16+

### 安装步骤

1. 克隆仓库
```bash
git clone https://github.com/your-org/T119-Cloud-Xplorers.git
cd T119-Cloud-Xplorers
```

2. 配置环境变量
```bash
cp .env.example .env
# 编辑 .env 文件，填入必要的配置信息
```

3. 启动服务
```bash
docker-compose up -d
```

## 项目结构

```
T119-Cloud-Xplorers/
├── docker/                # Docker 相关配置
├── src/                   # 源代码
│   ├── models/           # 模型定义
│   ├── services/         # 业务服务
│   └── utils/            # 工具函数
├── data/                 # 数据文件
├── configs/              # 配置文件
├── scripts/              # 脚本文件
└── docs/                 # 文档
```

## 模型训练

### ChatGLM 微调

1. 准备训练数据
2. 配置训练参数
3. 执行训练脚本

```bash
cd scripts
python train_model.py --config ../configs/train_config.yaml
```

## API 文档

API 文档可在服务启动后访问：`http://localhost:3000/docs`

## 配置说明

主要配置项包括：

- FastGPT 相关配置
- Azure OpenAI 配置
- Docker 环境配置
- 模型参数配置

## 部署指南

### Docker 部署

```bash
# 构建镜像
docker build -t cathay-travel-ai .

# 运行容器
docker run -d -p 3000:3000 cathay-travel-ai
```

### 生产环境配置建议

- 使用 Docker Compose 进行服务编排
- 配置负载均衡
- 设置监控和日志收集
- 实施备份策略

## 贡献指南

1. Fork 本仓库
2. 创建特性分支
3. 提交变更
4. 发起 Pull Request

## 许可证

[MIT License](LICENSE)

## 联系方式

- 项目维护者：[Your Name]
- 邮箱：[Your Email]

## 致谢

感谢以下项目和团队的支持：

- FastGPT 团队
- ChatGLM 开发团队
- Azure OpenAI 团队
