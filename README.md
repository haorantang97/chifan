<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/hero-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="assets/hero-light.png">
  <img src="assets/hero-light.png" alt="吃饭 Skill / Let’s Eat — LAB 305 出品的餐厅筛选 Skill" width="1000">
</picture>

**中文** · [English](README.en.md)

[![Lab 305](https://img.shields.io/badge/LAB_305-Let%E2%80%99s_Eat-123e5a?style=flat-square)](https://github.com/haorantang97) [![Agent Skill](https://img.shields.io/badge/Agent-Skill-d8462d?style=flat-square)](SKILL.md) [![License](https://img.shields.io/badge/license-PolyForm_NC_1.0.0-b45309?style=flat-square)](LICENSE)

[开始使用](#开始使用) · [它会看什么](#它会看什么) · [使用示例](#使用示例) · [FAQ](#faq)

</div>

# 吃饭 Skill / Let’s Eat

**好好选店，好好吃饭。**

吃饭 Skill 是 Lab 305 的餐厅筛选工具。把餐厅、菜单或一份探店推荐交给 Agent，它会查看经营模式、食材与烹饪、主厨与推荐者的经验，帮你判断这顿饭值不值得考虑。

适合把好吃放在首位、对资本化与标准化出品比较挑剔的人。

## 开始使用

在 Codex 中说：

> 用 skill-installer 安装 https://github.com/haorantang97/chifan 的根目录 Skill，名称为 chifan。

安装后，在下一轮对话中输入：

> 用 `$chifan` 帮我看这家餐厅值不值得吃：[餐厅名、城市及官网或菜单]。

也可以手动安装。需要 Git，且目标文件夹尚不存在：

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/haorantang97/chifan.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/chifan"
```

通过 Git 克隆安装后，可在该目录运行 `git pull --ff-only` 更新。Skill 本身不安装搜索服务；需要查询当前资料时，使用宿主 Agent 已有的搜索或浏览能力。

## 它会看什么

| 你关心的事 | 它会看 | 帮你判断 |
| --- | --- | --- |
| 这家店靠什么吸引人？ | 餐饮集团、品牌关联、连锁与名厨资本、经营场所 | 经营模式是否在压低食物的上限 |
| 菜单花哨，吃起来会怎样？ | 食材出处与品质、菜肴设计、实际掌厨、精密烹饪 | 菜品是否有支撑其定位与价位的东西 |
| 名厨和探店推荐可信吗？ | 主厨的训练、岗位与持续学习；推荐者的饮食阅历、复吃与分析能力 | 履历和赞美有多少参考价值 |

完整筛选会综合这三个方面；只问一道菜、主厨履历或一份推荐时，使用相关部分。食材、设计与烹饪可以相互补足，不要求每项都优秀。

## 使用示例

### 几家店里挑一家

> 用 `$chifan` 比较这三家餐厅。我们更在意食物，人均预算 ¥500。先说你会选哪家，再说影响选择的依据。餐厅与菜单如下：……

### 看一份高价菜单

> 用 `$chifan` 分析这份菜单：食材能否撑起价格，设计有什么值得注意的地方，主厨实际参与到什么程度？我附上了菜单和主厨介绍。

下面用一组虚构资料展示输出方式：

**输入**：一家人均 ¥800 的餐厅，菜单写“优质和牛”，未列产地和品种；主厨介绍只有“名店研修”，未说明时长或岗位；探店内容只有摆盘照片和“惊艳”的评价。

**输出示意**：按食物优先的筛选偏好，我会避开这家。高价菜单缺少具体的食材说明，研修头衔没有交代实际训练，推荐也没有分析食物好在哪里。这些资料不足以支撑它的价位与定位。

### 看一份探店推荐

> 用 `$chifan` 看这份推荐值不值得参考。重点看它有没有解释食材、技法和组合效果，以及推荐者有没有足够的比较经验。以下是推荐内容和公开资料：……

结果会先给选择建议，再说明具体依据和资料缺口。照片中的分析不会写成亲身试吃。

## FAQ

**它会替我订餐厅吗？** 这个 Skill 负责选择和分析，输出判断与理由。

**只能查某个平台吗？** 可以跨平台查餐厅官网、菜单和公开资料，也可以直接分析你给的文字或图片。能否打开某个页面取决于宿主 Agent 的工具和访问条件。

**它的口味是什么？** 食物优先，对资本化、连锁和标准化出品从严。规则也包含具体地区的取舍和个别品牌例外，可以在 [SKILL.md](SKILL.md) 中阅读全文。

**有英文版吗？** [English README](README.en.md) 提供完整的英文介绍。执行规则统一维护在中文 `SKILL.md` 中。

## 文件与验证

[SKILL.md](SKILL.md) 是完整规则入口；[agents/openai.yaml](agents/openai.yaml) 提供 Codex 显示名与默认提示词。`assets/` 保存品牌视觉与设计说明。

已完成 Skill 格式、规则合并、文件链接及 README 渲染检查。实际餐厅选择效果尚未经过真实用餐结果验证。

## 参与改进

欢迎报告规则歧义、过时信息和实际使用问题。提交方式见 [贡献说明](CONTRIBUTING.md)。

## 许可与 Lab 305

采用 [PolyForm Noncommercial 1.0.0](LICENSE)，允许非商业使用、修改和分发；商业使用需另行取得许可。

更多 Lab 305 工具：[LabKit](https://github.com/haorantang97/LabKit) · [Personal-Ontology](https://github.com/haorantang97/Personal-Ontology)
