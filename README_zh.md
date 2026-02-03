# Nature Figure Prompts

**[English](README.md) | 中文**

一个用于生成 Nature/Cell 期刊质量科学配图提示词的 Claude Code 技能。

## 概述

本技能帮助研究人员生成详细的 AI 图像生成提示词，用于创建符合高影响因子期刊（Nature/Cell/Science）发表标准的科学配图。

## 适用范围

**研究类型：**
- 因子试验 → 因子矩阵图
- 剂量效应研究 → 剂量响应曲线
- 机制研究 → 分子通路图
- 比较研究 → 并列对比图

**研究领域：**
- 生物医学（代谢、基因表达、信号通路）
- 农业科学（动物/植物营养、生长研究）
- 药理学（药物效应、毒理学）
- 免疫学（炎症反应、免疫通路）

**分析层次：**
- 整体层（生长、存活、性能指标）
- 组织/器官层（组织学、酶活性）
- 分子层（基因表达、蛋白水平、代谢物）

## 功能特点

- **论文分析框架**：系统性提取研究核心要素
- **配图规划**：根据论文内容决定配图类型
- **提示词模板**：预配置的常用配图类型模板：
  - 图文摘要 (Graphical Abstract)
  - 实验设计图
  - 代谢通路图
- **颜色标准**：色盲友好的调色板，含具体 HEX 值
- **质量检查清单**：确保配图符合发表标准

## 依赖项

本技能**仅生成提示词**。要根据这些提示词创建实际图像，您需要：

- **[scientific-schematics](https://github.com/K-Dense-AI/claude-scientific-skills/tree/main/scientific-skills/scientific-schematics)** - 基于 AI 的图像生成，使用 Nano Banana Pro 生成图像，Gemini 3 Pro 进行质量评审。支持智能迭代优化，根据文档类型设置不同的质量阈值（期刊论文: 8.5/10，海报: 7.0/10 等）

> **注意：** 需要 [OpenRouter API 密钥](https://openrouter.ai/keys) 才能使用 AI 图像生成功能。

从 [claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) 安装依赖：

```bash
# 克隆 scientific-skills 仓库
git clone https://github.com/K-Dense-AI/claude-scientific-skills.git

# 将 scientific-schematics 复制到技能目录
cp -r claude-scientific-skills/scientific-skills/scientific-schematics .claude/skills/
```

## 安装

将技能复制到 Claude Code 技能目录：

```bash
# 如果目录不存在则创建
mkdir -p .claude/skills

# 复制技能
cp -r nature-figure-prompts .claude/skills/
```

## 使用方法

在 Claude Code 中使用：

```
/nature-figure-prompts <论文路径>
```

或者直接提供论文内容：
```
帮我为这篇论文创建配图：[论文内容或路径]
```

## 目录结构

```
nature-figure-prompts/
├── SKILL.md                    # 主技能定义文件
└── references/
    ├── paper-analysis.md       # 论文分析框架
    ├── layouts.md              # 布局模板（4种类型）
    ├── colors.md               # 颜色标准和 HEX 值
    ├── vocabulary.md           # 英文术语表
    └── troubleshooting.md      # 常见问题修复和迭代技巧
```

## 视觉风格指南

所有生成的提示词遵循以下标准：
- Nature/Cell 期刊质量
- 带柔和阴影的立体 3D 元素
- 干净的灰白色背景 (#FAFAFA)
- 专业排版（基因名斜体）
- 色盲友好调色板 (Okabe-Ito)

## 颜色约定

- **上调**：红色 (#E53935) 配 ↑ 箭头
- **下调**：绿色 (#43A047) 配 ↓ 箭头
- **糖代谢**：绿色 (#4CAF50)
- **脂代谢**：橙色 (#FF9800)
- **蛋白代谢**：蓝色 (#2196F3)
- **免疫反应**：红色 (#F44336)

## 贡献

欢迎贡献！请随时提交 Issue 或 Pull Request。

## 许可证

MIT 许可证

## 致谢

- 参考 Nature/Cell 出版指南
- 颜色方案基于 Okabe-Ito 色盲安全调色板
