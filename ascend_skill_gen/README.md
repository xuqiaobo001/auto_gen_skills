# Ascend Skill Gen

Huawei Ascend NPU 相关的 Claude Code Skills 集合，基于 ModelArts 官方用户指南文档生成，覆盖 Standard、Lite Server、Lite Cluster 三大产品形态。

## 目录结构

```
ascend_skill_gen/
├── README.md
├── modelarts_standard_usermanual_toc.md        # Standard 用户指南目录 (数据源)
├── modelarts_lite_server_usermanual_toc.md      # Lite Server 用户指南目录 (数据源)
├── modelarts_lite_cluster_usermanual_toc.md     # Lite Cluster 用户指南目录 (数据源)
├── ma_standard_skills/                          # ModelArts Standard Skills (9个)
├── ma_lite_devserver_skills/                    # ModelArts Lite Server Skills (9个)
└── ma_lite_cluster_skills/                      # ModelArts Lite Cluster Skills (7个)
```

## Skills 概览

共计 **25** 个 Skills，覆盖 ModelArts 三大产品形态的完整用户指南。

### ModelArts Standard Skills (9个)

基于 [ModelArts Standard 用户指南](https://support.huaweicloud.com/intl/zh-cn/usermanual-standard-modelarts/) 生成。

| Skill | 说明 |
|---|---|
| `ascend-resource-pool` | 管理 Ascend NPU 专属资源池的创建、扩缩容、升级和故障修复 |
| `ascend-notebook-dev` | 在 Ascend NPU 上创建和使用 Notebook 开发环境 (JupyterLab/PyCharm/VS Code) |
| `ascend-image-builder` | 构建适用于 Ascend NPU 的自定义 Docker 训练/推理镜像 |
| `ascend-training-code-migration` | 将 GPU 训练代码迁移到 Ascend NPU (torch_npu 适配、算子兼容) |
| `ascend-distributed-training` | 配置和运行 Ascend NPU 分布式训练 (PyTorch DDP + HCCL) |
| `ascend-training-reliability` | 配置高可靠训练：断点续训、自动故障恢复、训练挂起检测 |
| `ascend-inference-deploy` | 在 Ascend NPU 上部署模型推理服务 (在线/批量推理) |
| `ascend-monitoring` | NPU 资源监控与告警 (Grafana、AOM、CES) |
| `ascend-workflow-builder` | 使用 ModelArts Workflow 构建端到端 AI 流水线 |

### ModelArts Lite Server Skills (9个)

基于 [ModelArts Lite Server 用户指南](https://support.huaweicloud.com/intl/zh-cn/usermanual-server-modelarts/) 生成。

| Skill | 说明 |
|---|---|
| `lite-server-quickstart` | Lite Server 入门：使用前提、流程概览、高危操作、计算-镜像兼容性、资源开通 |
| `lite-server-network-storage` | 网络配置 (VPC)、存储配置 (EVS/SFS)、软件环境安装 |
| `lite-server-model-adaptation` | LLM/AIGC 模型 NPU 训练推理适配、GPT-2 GPU 训练推理 |
| `lite-server-lifecycle` | 服务器全生命周期管理：开关机、OS 切换/重置、热备、授权维修 |
| `lite-server-plugin` | 插件管理：AI 插件安装、Ascend 驱动固件升级、CES Agent |
| `lite-server-node-ops` | 节点运维：故障诊断、漏洞修复、一键压测、参数面网络配置 |
| `lite-server-supernode` | 超节点管理：扩缩容、系统盘扩容、定期压测、HCCL 算子级重执行 |
| `lite-server-monitoring` | 日志采集 (NPU/GPU)、CES 监控告警、DCGM GPU 监控 |
| `lite-server-audit` | CTS 审计、CloudPond NPU 资源管理、资源退订 |

### ModelArts Lite Cluster Skills (7个)

基于 [ModelArts Lite Cluster 用户指南](https://support.huaweicloud.com/intl/zh-cn/usermanual-cluster-modelarts/) 生成。

| Skill | 说明 |
|---|---|
| `lite-cluster-quickstart` | Lite Cluster 入门：使用流程、高危操作、软件版本兼容、资源开通 |
| `lite-cluster-configuration` | 资源配置：网络、kubectl、存储 (SFS Turbo/OBS)、驱动、镜像预热 |
| `lite-cluster-distributed-training` | 分布式训练：Snt9B 训练、ranktable PyTorch NPU 训练、Volcano 调度 |
| `lite-cluster-inference-and-tools` | 推理部署、Ascend FaultDiag 诊断、SFS Turbo 挂载、HA 冗余节点、跨区域访问 |
| `lite-cluster-resource-management` | 资源管理：资源池/节点池/节点管理、弹性扩缩容、驱动升级 |
| `lite-cluster-monitoring` | AOM/Prometheus 监控、资源释放 |
| `lite-cluster-plugin` | 插件管理：Node Agent、Metrics Collector、Device Plugin、Volcano、弹性引擎 |

## Skill 文件格式

每个 Skill 目录包含两个文件：

```
<skill-name>/
├── SKILL.md       # Skill 定义文件
└── LICENSE.txt    # Apache 2.0 许可证
```

`SKILL.md` 遵循 Claude Code Skills 标准格式：

```markdown
---
name: skill-name
description: Skill 描述及触发条件
license: Apache 2.0
---

# Skill 标题

## Overview
简要说明

## When to Use
- 触发场景列表

## [技术内容章节]
表格、代码示例、操作步骤等

## Reference Documentation
- [文档链接](url)
```

## 数据源

Skills 基于以下华为云官方文档目录生成：

| 数据源文件 | 文档来源 | 条目数 |
|---|---|---|
| `modelarts_standard_usermanual_toc.md` | [ModelArts Standard 用户指南](https://support.huaweicloud.com/intl/zh-cn/usermanual-standard-modelarts/) | — |
| `modelarts_lite_server_usermanual_toc.md` | [ModelArts Lite Server 用户指南](https://support.huaweicloud.com/intl/zh-cn/usermanual-server-modelarts/) | 50 |
| `modelarts_lite_cluster_usermanual_toc.md` | [ModelArts Lite Cluster 用户指南](https://support.huaweicloud.com/intl/zh-cn/usermanual-cluster-modelarts/) | 40 |

## 许可证

所有 Skills 均采用 [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) 许可证。
