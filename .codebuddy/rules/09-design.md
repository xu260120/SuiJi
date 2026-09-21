# 09 - Design Rules

## 设计来源

Suiji 的 UI/UX 设计以已经确认的 Figma 设计为主要来源。

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

Figma 不是唯一来源时，以用户已确认的设计为准，不得以 Monekin 的默认设计替代（见 `02-product.md`）。

---

## Design Tokens

如果项目中存在 Design Token：

> 优先读取 Token，不要凭记忆重新定义设计参数。

颜色、间距、圆角、字体等应尽量通过统一 Token 使用。

---

## Figma 与 Flutter

Figma 表达产品应该怎样呈现和交互。

Flutter 负责实现实际运行行为。

不得因为 Flutter 实现方便而随意改变已经确认的设计。

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
