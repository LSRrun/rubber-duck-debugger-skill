# 橡皮鸭苏格拉底式调试助手

Claude Code 技能。一只不直接给你答案、而是通过反问引导你自己找到 bug 根因的橡皮鸭。

## 安装

```bash
git clone https://github.com/LSRrun/rubber-duck-debugger.git ~/.claude/skills/rubber-duck-debugger
```

## 使用方式

用 Claude Code 时描述你遇到的 bug：

```
> /rubber-duck-debugger 调用 /api/payment 报了 NullPointerException
```

橡皮鸭会：
1. 🔍 **追问症状** — 引导你找到异常堆栈、确认复现条件
2. 🎯 **缩小范围** — 二分法帮你定位到具体模块或代码行
3. 💡 **挑战假设** — 追问你觉得"不可能"的前提是否真的成立
4. 🧪 **设计实验** — 帮你用最小的改动验证假设
5. 📝 **复盘总结** — 修好了？花 30 秒想想下次怎么避免

**随时可以说"直接告诉我答案"退出引导模式。**

## 什么场景下用它

- 遇到 bug 想训练自己的调试思维，而不是复制粘贴答案
- 问题排查卡住了，需要一个"橡皮鸭"来问对的问题
- 想建立系统化的调试习惯（复现 → 隔离 → 假设 → 验证 → 复盘）

## 文件结构

```
.
├── SKILL.md                    # 核心工作流与规则
└── references/
    ├── debug-stages.md         # 五阶段调试流程 + 提问模板
    ├── question-patterns.md    # 五种提问类型 + 示例
    └── escape-hatch.md         # 退出机制与提醒规则
```

## 许可

MIT
