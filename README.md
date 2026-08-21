# Skills

个人 Agent 技能库。把重复的专业流程封装成可触发、可复用的能力包。

## 技能列表

### 学习系统

> 基于 [How To Learn Anything 10x Faster Using Claude](https://x.com/sairahul1/article/2068250224532050089) 提炼。

| 技能 | 说明 | 触发场景 |
|------|------|----------|
| [`learn-10x`](skills/learn-10x/) | 学习路由器，调度其他 6 个学习技能 | "我想学 X" |
| [`signal-in-noise`](skills/signal-in-noise/) | 从海量资源中筛选 5 个最高杠杆的学习材料 | "帮我找资源" |
| [`learning-ladder`](skills/learning-ladder/) | 将任意主题拆分为 5 级难度路径，附带里程碑和自测 | "我该从哪开始" |
| [`20-hour-plan`](skills/20-hour-plan/) | 提取核心 20%，生成 10 次 × 2 小时的学习计划 | "帮我制定学习计划" |
| [`quiz-me`](skills/quiz-me/) | 一问一答式主动回忆测验，定位知识缺口 | "考考我" |
| [`cheat-sheet`](skills/cheat-sheet/) | 将主题压缩为一页速查表 | "做个总结" |
| [`feynman-loop`](skills/feynman-loop/) | 费曼技巧：用简单语言解释，发现缺口后重新教学 | "解释 X" |

<!-- 其他类别技能请按相同格式追加在此处 -->

## 目录结构

```
skills/
├── README.md
└── skills/
    ├── learn-10x/
    │   └── SKILL.md
    ├── signal-in-noise/
    │   └── SKILL.md
    ├── learning-ladder/
    │   └── SKILL.md
    ├── 20-hour-plan/
    │   └── SKILL.md
    ├── quiz-me/
    │   └── SKILL.md
    ├── cheat-sheet/
    │   └── SKILL.md
    └── feynman-loop/
        └── SKILL.md
```

## 使用方式

每个技能独立可用，也可通过路由器串联。

直接调用：
```
/quiz-me JavaScript 闭包
/cheat-sheet 线性代数
```

通过路由器：
```
/learn-10x 机器学习
```

## 技能格式

遵循 [Agent Skills 规范](https://github.com/anthropics/skills)：

- `SKILL.md` — 必需，frontmatter（name + description）+ 工作流指令
- `references/` — 可选，详细参考资料
- `scripts/` — 可选，确定性脚本
