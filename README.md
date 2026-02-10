# Auto Gen Skills

从开源项目源码与云服务官方文档中自动提炼的 **Claude Code Skills** 集合。每个技能以结构化 Markdown 文件呈现，可供开发者学习参考，也可作为 AI 编程助手的上下文知识加载使用。

## 项目理念

优秀的开源项目蕴含大量经过生产验证的架构模式与工程实践，云服务文档则包含丰富的运维操作指南。本项目通过 AI 辅助分析，将这些知识提炼为独立、可复用的 Claude Code Skill 文件，降低学习门槛，提升开发效率。

## 目录结构

```
auto_gen_skills/
├── dify_gen_skill/                      # Dify — 开源 LLM 应用平台（17 个技能）
│   ├── flask-ddd-scaffold/              #   Flask DDD 分层架构脚手架
│   ├── multi-tenant-rbac/               #   多租户 RBAC 权限体系
│   ├── jwt-multi-auth/                  #   JWT 多策略认证
│   ├── repository-factory/              #   Repository Factory 数据访问层
│   ├── celery-async-tasks/              #   Celery 异步任务框架
│   ├── pydantic-config-management/      #   Pydantic 配置管理
│   ├── flask-blueprint-api/             #   Flask Blueprint 多 API 域
│   ├── otel-observability/              #   OpenTelemetry 可观测性
│   ├── domain-error-hierarchy/          #   领域异常层次体系
│   ├── plugin-extension-system/         #   插件化扩展体系
│   ├── nextjs-enterprise-scaffold/      #   Next.js 企业级脚手架
│   ├── orpc-contract-first-api/         #   oRPC 契约优先 API
│   ├── multi-layer-state-management/    #   多层状态管理
│   ├── i18n-namespace-system/           #   i18n 命名空间体系
│   ├── tailwind-component-system/       #   Tailwind + CVA 组件系统
│   ├── docker-compose-fullstack/        #   Docker Compose 全栈部署
│   └── event-driven-architecture/       #   事件驱动架构
├── ascend_skill_gen/                    # 华为 Ascend NPU & ModelArts（25 个技能）
│   ├── ma_standard_skills/              #   ModelArts Standard Skills（9 个）
│   ├── ma_lite_devserver_skills/        #   ModelArts Lite Server Skills（9 个）
│   └── ma_lite_cluster_skills/          #   ModelArts Lite Cluster Skills（7 个）
└── README.md
```

每个 skill 目录遵循标准 Claude Code Skill 格式：

```
<skill-name>/
├── SKILL.md        # 技能定义（含 YAML frontmatter: name, description, version, license）
└── LICENSE.txt     # Apache 2.0 许可证
```

## 已收录项目

| 项目 | 目录 | 技能数 | 涵盖领域 |
|------|------|--------|----------|
| [Dify](https://github.com/langgenius/dify) | `dify_gen_skill/` | 17 | Flask DDD 架构、多租户 RBAC、JWT 认证、Repository Factory、Celery 异步任务、Pydantic 配置、Blueprint API、OpenTelemetry 可观测、领域错误层级、插件系统、Next.js 脚手架、oRPC 契约 API、多层状态管理、i18n、Tailwind 组件、Docker Compose 部署、事件驱动架构 |
| [Huawei Ascend / ModelArts](https://support.huaweicloud.com/intl/zh-cn/usermanual-standard-modelarts/) | `ascend_skill_gen/` | 25 | NPU 资源池管理、Notebook 开发、自定义镜像构建、GPU→NPU 代码迁移、分布式训练 (HCCL/Volcano)、高可靠训练、推理部署、监控告警、Workflow 流水线、Lite Server 运维、Lite Cluster K8s 管理、插件管理 |

> 后续将持续收录更多项目的技能。

## 技能文件规范

每个技能文件遵循 Claude Code Skill 标准格式，根据来源不同侧重点有所区别：

### 开源项目架构技能（如 Dify）

- **核心模式** — 关键设计模式与架构决策
- **代码示例** — 从源码中提取的真实代码片段
- **关键规则** — 使用该模式时必须遵守的约束
- **反模式** — 常见的错误用法与应避免的做法

### 云服务运维技能（如 Ascend / ModelArts）

- **Overview** — 技能概述与适用范围
- **When to Use** — 触发场景列表
- **操作指南** — 分步骤操作说明、命令示例、配置模板
- **Reference Documentation** — 官方文档链接

## 使用方式

### 1. 作为 Claude Code Skills 加载

将技能文件加载到 Claude Code 中，AI 助手将自动获得对应领域的专业知识，辅助完成开发与运维任务。

### 2. 作为学习材料

阅读各项目的技能文件，系统性学习架构模式与云服务运维实践。

### 3. 作为架构参考

在构建新项目或管理云资源时，参考已收录的设计模式与操作指南。

## 贡献

欢迎为本仓库贡献新的技能提炼，请遵循现有的目录组织方式：

1. 创建 `<project>_gen_skill/` 目录
2. 每个技能创建独立子目录，包含 `SKILL.md` 和 `LICENSE.txt`
3. `SKILL.md` 使用 YAML frontmatter（name, description, license）
4. 为项目目录编写 `README.md` 说明

## 许可证

所有 Skills 均采用 [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) 许可证。
