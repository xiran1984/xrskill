# xrskill

一组帮助 Agent 处理目标拆解、行动选择和心理卡点的 Skills。

## 是什么

| Skill | 适合解决的问题 | 调用命令 |
| --- | --- | --- |
| `xr-goal` | 目标已经明确，但不知道实现条件、当前瓶颈或下一步 | `/xr-goal` |
| `xr-survive-game` | 不知道一件事值不值得做，或能量太低、无法启动 | `/xr-survive-game` |
| `xr-trauma-support` | 知道该做什么，却被恐惧、羞耻、无助感或旧经历形成的保护策略卡住 | `/xr-trauma-support` |

`xr-trauma-support` 的目的，是处理一部分行动瘫痪背后的心理原因。它采用“创伤识别—情绪宽慰—解决方法”三步对话；稳定后可接入 `xr-goal`，把恢复方向转化为安全、可执行的行动路径。

## 怎么选择

```text
目标明确，只缺实现路径                 → xr-goal
方向不清，不知道是否值得继续           → xr-survive-game
知道该做什么，却因心理反应反复卡住     → xr-trauma-support
心理卡点缓解后，需要系统行动方案       → xr-trauma-support → xr-goal
```

## 怎么安装

下载这些 Skills：[xiran1984/xrskill](https://github.com/xiran1984/xrskill)

## 怎么用

直接输入命令和你的问题：

```text
/xr-goal 我想在三个月内完成一个可以公开使用的 AI 工具
/xr-survive-game 我一直在研究个人 IP，却没有实际产出，还值得继续吗？
/xr-trauma-support 我知道应该开始，但一想到失败就会僵住并责备自己
```

也可以直接用自然语言描述问题。部分 Agent 客户端使用 `$xr-goal`、`$xr-survive-game` 和 `$xr-trauma-support` 作为显式调用格式。

## 私人档案

公开仓库只提供空白模板。每个 Agent 在本地创建自己的 `xr-trauma-support/private/user-patterns.md` 和 `xr-survive-game/memory/`；这些私人文件默认被 Git 忽略，未经用户明确同意不应记录。

## 安全边界

`xr-trauma-support` 只用于初筛、自助支持和现实功能恢复，不替代诊断或专业治疗，也不进行记忆恢复、催眠、自行暴露治疗或停药指导。遇到自伤、伤人、现实暴力、严重戒断或无法保证安全的情况，应停止分析并优先连接现实中的紧急与专业支持。

## 仓库结构

```text
xrskill/
├─ xr-goal/             # 因果条件树与执行路径
├─ xr-survive-game/     # 意义评估与五分钟行动导航
└─ xr-trauma-support/   # 心理卡点、创伤初筛与自助支持
```

## License

请在使用或分发前确认仓库中的许可证与第三方资料许可。参考文件只保存原创转述、适用条件与安全边界，不复制受版权保护的完整材料。
