# 05 - Monekin Reference Rules

## Monekin 的定位

Monekin（AGPL-3.0）是 Suiji 的：

- 学习参考项目
- 产品理念参考
- 技术思路参考

Monekin 不是 Suiji 的：

- 代码来源
- 技术基础
- 需要跟随的上游
- Suiji 的上游项目

---

## 独立实现边界

Suiji 的代码全部自行实现。

Monekin 的代码、文件结构、数据库 Schema、美术资产不得进入 Suiji 仓库。

---

## 项目层次与参考目录

**Suiji（随记账）是用户自己的项目**，不是任何外部项目的分支、衍生或延续。

必须区分三层，不得混用：

1. **产品项目**：`D:\lx\Desktop\suijiProject\suiji`，Suiji 唯一产品仓库，独立 Git 仓库，origin 为 `https://github.com/xu260120/SuiJi.git`；分支模型见 `06-git.md`，本文件不复述。
2. **外部参考**：GitHub 上的 Monekin 开源仓库 `https://github.com/enrique-lozano/Monekin`（AGPL-3.0），是外部项目，不是 Suiji 的组成部分、上游项目（upstream）或 Git 远程（remote）。
3. **本地只读副本**：`D:\lx\Desktop\suijiProject\monekin-ref`，上述外部仓库的克隆副本，自带 `.git` 的独立仓库，仅用于学习、分析和比较。

本地副本与 `suiji/` 同处 `suijiProject/` 工作区根目录：**在 suiji 仓库之外，但在同一工作区内**。

工作区根目录本身不是 Git 仓库，`suiji/` 与 `monekin-ref/` 各是独立仓库。在根目录执行 git 命令前必须确认作用域，不得误把参考副本当作 Suiji 仓库操作，也不得据此推断两者存在 Git 关系。

Monekin 与本地副本都不参与 Suiji 的依赖、代码、Schema、资源、项目结构与版本管理；参考目录不属于 Suiji 仓库，也不进入 Suiji Git 历史。

不得将其作为 package、path 依赖或任何形式引入 `pubspec.yaml`。

不得将其中任何文件复制进 Suiji 工作区。

---

## 允许的学习内容

- 功能范围与产品定位
- 页面结构、导航与交互设计
- 记账类型与核心流程设计
- 技术选型（drift、fl_chart 等公开通用库）
- 大致的数据与模块划分思路

即使只借鉴思路而未复制代码，也须按 `08-ai-behavior.md`「非自主开发内容的参考来源」标注参考来源。

---

## 禁止事项

未经用户确认，不得：

- 复制 Monekin 的代码或注释
- 照搬 Monekin 的文件结构、类结构设计
- 复制 Monekin 的数据库 Schema 或表结构定义
- 使用 Monekin 的图标、图片、配色等美术资产
- 把 Monekin 源码放入 Suiji 仓库或克隆进 Suiji 目录
- 将 Monekin 作为 Suiji 的上游项目

---

## 相似度判断

如果某处实现与 Monekin 高度相似：

- 先判断是否属于记账类 App 的通用做法
- 属于通用做法 → 可以自行正常实现
- 属于 Monekin 特有表达 → 必须改用 Suiji 自己的实现

Suiji 的目标是：

> 即使完全不看 Monekin 代码，Suiji 依然完整成立。

---

## 学习 Monekin 更新的方式

Monekin 未来发布新版本或改动时：

- 作为学习材料阅读
- 只吸收理念、设计与思路上的参考价值
- 不吸收任何代码

是否拉取、何时拉取、拉取到哪个版本由用户决定。

CodeBuddy 不得自动向参考目录拉取或写入。

---

## License

涉及 Monekin 许可证、代码使用、衍生作品、发布义务等问题时：

- 区分已确认事实与法律判断
- 不得把 AI 推测描述为法律结论
- 必要时进一步核对许可证原文或寻求专业意见

参考 Monekin 或任何开源产品前，按 `08-ai-behavior.md`「版权与许可：第一时间告知」主动向用户说明版权与许可风险；参考了什么按同文件「非自主开发内容的参考来源」标注来源。本节只规定判断口径，不另定义告知时序与标注规则。

---

## 产品决策

Monekin 中存在的功能不代表 Suiji 必须拥有。

AI 不得因为 Monekin 已经实现某功能，就自动把该功能加入 Suiji。

---

## 核心原则

> Monekin 是参考书，不是地基。

> Suiji 可以向 Monekin 学习，但代码必须由 Suiji 自己写。
