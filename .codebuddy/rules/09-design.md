# 09 - Design Rules

## 设计依据

Suiji 的页面结构、布局与交互以**用户已确认的设计产物**为准；颜色取值以项目 Color Tokens 为准（见下节）。

页面视觉效果可以由 AI 或专家团队产出草案，但未经用户确认不得视为已确认设计，也不得直接落地为最终实现。

这类草案属于非自主开发内容，按 `08-ai-behavior.md`「非自主开发内容的参考来源」标注来源并在报告中呈现。

没有已确认的设计产物时，不得凭记忆、通用模板或参考项目的默认样式自行定义设计参数；应先提出方案并等待确认。

不得以 Flutter 实现方便为由改变已确认的设计。

## 设计范围

设计范围包括：

- 页面结构
- 布局
- 组件
- 颜色
- 字体
- 间距
- 圆角
- 状态
- Light / Dark Theme
- Design Tokens

---

## Design Tokens

项目 Color Tokens 位于 suiji 仓库之外的工作区根目录，**未被 Git 跟踪**：

```text
D:\lx\Desktop\suijiProject\记账App_Color_Tokens_Light.json
D:\lx\Desktop\suijiProject\记账App_Color_Tokens_Dark.json
D:\lx\Desktop\suijiProject\记账App_Color_Tokens_Reference.json
```

- `Light` / `Dark`：Light / Dark 主题下各语义色的取值，使用 DTCG `$value` 结构。
- `Reference`：同一组色值的 Light / Dark 对照表，结构为 `{light, dark}`，用于逐项核对一致性。

> 优先读取 Token，不要凭记忆重新定义设计参数。

颜色、间距、圆角、字体等应尽量通过统一 Token 使用。

三份文件出现色值不一致时，不自行择一：指出差异并等待用户确认（见 `01-project.md`）。改动 Token 时必须同步更新三份文件并复核一致性。

这三份文件不在 suiji 仓库内。克隆仓库或在新环境工作时须先确认它们是否存在；不存在时明确告知用户，不得凭记忆补造色值。

---

## 设计冲突

如果设计与代码冲突：

1. 指出冲突
2. 说明具体差异
3. 判断属于设计问题还是实现问题
4. 需要产品决策时等待用户确认

---

## 语义颜色

账务颜色必须遵守已确认的语义：

- 收入使用 Income
- 支出使用 Expense
- 转账使用 Transfer
- Brand 用于品牌和主要交互状态

不得把品牌色随意当作收入、支出或转账颜色。

颜色不能成为唯一的信息表达方式。

---

## 与 Monekin 的关系

可以参考 Monekin 的布局思路和交互思路。

但不得直接使用 Monekin 的图标、图片、配色等美术资产（见 `05-monekin.md`）。

---

## 设计变更

大范围 Design Token 变化属于中风险变更，按 `11-change-control.md` 先分析影响。
