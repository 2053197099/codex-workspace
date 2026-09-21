# 电影视觉提示词 Skills

本项目把人物、场景参考和创作意图整理成可复用的电影视觉设定与空间故事。

## 使用入口

| 请求 | 入口 |
| --- | --- |
| 完整视觉方案、系列提示词、空间故事 | [cinematic-visual-bible](.skills/cinematic-visual-bible/SKILL.md) |
| 仅摄影参数、光影、胶片色彩 | [cinematic-look-design](.skills/cinematic-look-design/SKILL.md) |
| 仅场景布局、美术与路线 | [cinematic-space-design](.skills/cinematic-space-design/SKILL.md) |
| 仅动作、主客观视角、运镜或分镜 | [cinematic-sequence-design](.skills/cinematic-sequence-design/SKILL.md) |

总控按需求读取专业模块，不要求多代理或每次加载全部资料。默认交付明确、精简的成品；内部工作卡、选型候选和审核过程不进入正文。完整空间故事扩展有连接与行动价值的相邻区域，静态复刻保持指定边界。

## 资料分层

- Skills 下的 `references/`：按需加载的摄影交付规则、胶片证据、技术核对、具名预设和维护用案例。
- [摄影参数与视觉机制库](cinematography-library/摄影参数与视觉机制库.md)：需要比较机制、查场景选型条件时读取；不把整库当通用提示词。
- [初始逆向报告](cinematic-skills-reconstruction.md)与[迭代记录](cinematography-library/通用质感提示词迭代记录.md)：历史研究记录，不作为当前执行规则。
- [Git 协作维护](docs/git-multidevice.md)：仓库维护参考，不参与创作流程。项目约束以 [AGENTS.md](AGENTS.md) 为准。

`.skills/` 是本项目维护源；本机使用的四个同名副本位于 `~/.codex/skills/`，修改后需同步并核对。其他全局 Skills 不属于本项目清理范围。

## 验证

修改后检查四个 Skill 的结构、相对引用、安装副本一致性，并按[回归案例](.skills/cinematic-visual-bible/references/validation-cases.md)验证受影响的交付分支。文本验证不代表生成画面已验收。
