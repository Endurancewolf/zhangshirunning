# CLAUDE.md — 跑酷小游戏项目工作指引

## 项目简介

这是一个 Windows 上的卡通风格跑酷小游戏。用户是不懂代码的小白。游戏为 HTML 单文件架构（`index.html`），双击即可在浏览器中游玩。

## 文档索引

项目规范文档统一放在 `docs/` 文件夹中，每次开发前请查阅：

| 文档 | 路径 | 内容 |
|------|------|------|
| 开发需求 | [docs/requirements.md](docs/requirements.md) | 游戏功能需求、角色设定、道具规则 |
| 技术规范 | [docs/technical-spec.md](docs/technical-spec.md) | 技术选型、架构、碰撞检测、参数表 |
| 设计规范 | [docs/design-spec.md](docs/design-spec.md) | 配色方案、外观尺寸、UI 布局 |
| 执行步骤 | [docs/execution-plan.md](docs/execution-plan.md) | 8 阶段任务清单和验收标准 |

## 工作约定

### 推进节奏
1. **严格遵守分阶段执行**，参考 [docs/execution-plan.md](docs/execution-plan.md)
2. **每次只推进一个阶段**，完成并验收后再进入下一阶段
3. **每阶段结束必须更新开发日志**，写入 `dev-logs/` 文件夹

### 开发日志规范
- 日志文件命名：`dev-logs/YYYY-MM-DD.md`
- 每次会话结束时更新当天日志
- 模板格式：
  ```markdown
  # YYYY-MM-DD 开发日志
  ## 今日完成
  - [x] 事项
  ## 遇到的问题
  ## 当前待办
  ## 下一步计划
  ```

### 代码风格
- 文件：单个 `index.html`，所有代码集中管理
- JavaScript：ES6+ 语法，函数 + 对象字面量组织模块
- 注释：关键逻辑用中文注释，方便用户理解
- 变量命名：驼峰命名法 `camelCase`
- 常量：大写蛇形命名法 `UPPER_SNAKE_CASE`（放在 CONFIG 对象中）

### 游戏参数
- 所有可调参数集中在 `CONFIG` 对象中，方便调参
- 关键参数参考 [docs/technical-spec.md](docs/technical-spec.md) 第 8 节

### 向用户沟通
- 用户不懂代码，解释时用通俗语言，不抛术语
- 每完成一个阶段，用简洁的中文告知用户做了什么、如何验收
- 出现问题时直接说明，不隐藏

## 项目文件结构

```
zhangshirunning/
├── index.html          # 游戏本体
├── CLAUDE.md           # 本文件
├── dev-logs/           # 开发日志
│   └── YYYY-MM-DD.md
└── docs/               # 规范文档
    ├── requirements.md
    ├── technical-spec.md
    ├── design-spec.md
    └── execution-plan.md
```
