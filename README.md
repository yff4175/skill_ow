# skill_ow

守望先锋工坊（Overwatch Workshop）代码编写规范技能包（ow-workshop-syntax）。

## 简介

本技能提供守望先锋工坊 `.ow` 代码的完整编写规范与权威参考，帮助编写、调试工坊规则。语法定义提取自 [XHanL/overwatch-workshop](https://github.com/XHanL/overwatch-workshop)（VS Code 扩展 v3.11+），并以真实工坊导出代码校正。

## 目录结构

| 文件 | 内容 | 用途 |
|---|---|---|
| `SKILL.md` | 技能主文件：完整编写规范 | 编写/调试工坊规则时的核心参考 |
| `工坊参数参考.md` | 参数格式参考（玩家验证版） | 常用动作的参数数量与格式速查 |
| `references/ow.tmLanguage.json` | TextMate 语法定义 | 所有动作/值/常量/事件/英雄的完整权威列表 |
| `references/SYMBOL_ACTION.js` | 动作定义示例 | 查看动作的参数结构、默认值、格式模板 |
| `references/SYMBOL_CONDITION.js` | 值/条件定义示例 | 查看值函数的参数、返回类型、格式 |
| `references/SYMBOL_CONSTANT.js` | 常量定义示例 | 查看比较运算符、队伍等常量 |

## 使用

编写或调试守望先锋工坊 `.ow` 代码时，调用本技能并遵循 `SKILL.md` 中的规范：

- 结构关键字使用中文（`规则`、`事件`、`条件`、`动作`、`变量`、`子程序`）
- 控制流关键字使用英文（`If`、`Else`、`End`、`While`、`For 全局变量`）
- 代码结构标点一律使用英文半角（`()` `,` `;` `"` `:`）
- 不确定的函数名、签名、参数数量时，优先查阅 `references/` 或向用户确认，禁止凭记忆猜测

## 数据来源

- 语法定义与符号数据：`XHanL/overwatch-workshop` 的 `syntaxes/ow.tmLanguage.json` 与 `src/web/model.ts`
- 完整数据源（未包含在本仓库中，体积较大）：[model.ts](https://raw.githubusercontent.com/XHanL/overwatch-workshop/main/src/web/model.ts)
