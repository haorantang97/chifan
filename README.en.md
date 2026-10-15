<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/hero-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="assets/hero-light.png">
  <img src="assets/hero-light.png" alt="Dinning Skill · 吃饭Skill — a restaurant-screening skill by LAB 305" width="1000">
</picture>

[中文](README.md) · **English**

[![Lab 305](https://img.shields.io/badge/LAB_305-Dinning-a31832?style=flat-square)](https://github.com/haorantang97) [![Agent Skill](https://img.shields.io/badge/Agent-Skill-333333?style=flat-square)](skills/dinning/SKILL.md) [![License](https://img.shields.io/badge/license-PolyForm_NC_1.0.0-333333?style=flat-square)](LICENSE)

[Get started](#get-started) · [What it looks at](#what-it-looks-at) · [Examples](#examples) · [FAQ](#faq)

</div>

# Dinning Skill

吃饭Skill

**Choose restaurants with care. Put food first.**

Dinning Skill is Lab 305's restaurant-screening skill. Give your agent a restaurant, a menu or a dining recommendation. It looks at the business behind the restaurant, its ingredients and cooking, and the experience of its chefs and reviewers to help you decide whether the meal is worth considering.

It is for people who put good food first and are particular about investor-driven restaurant businesses and standardized cooking.

## Get started

In Codex, say:

> Use skill-installer to install https://github.com/haorantang97/dinning/tree/main/skills/dinning

Once installed, use it on your next turn:

> Use `$dinning` to help me decide whether this restaurant is worth eating at: [restaurant name, city, and website or menu].

For manual installation, copy the repository's `skills/dinning/` folder into your Codex Skills directory (`~/.codex/skills/` by default). To update, replace the rules and configuration in that folder.

The skill uses the host agent's existing search or browsing tools when current information is needed.

## What it looks at

| Your question | What it examines | What it helps you judge |
| --- | --- | --- |
| What draws people to this restaurant? | Restaurant groups, related brands, chains, chef-led groups and the venue | Whether the business model limits how good the food can be |
| The menu looks impressive. How might the food taste? | Ingredient sources and quality, dish design, who actually cooks, and precision in cooking | Whether the food supports the restaurant's positioning and prices |
| Can I trust the chef's reputation or the recommendation? | The chef's training, kitchen roles and continued learning; the reviewer's dining experience, repeat visits and analysis | How much weight to give the credentials and praise |

A full assessment considers all three areas. If you ask about a single dish, a chef's background or a recommendation, it uses the relevant parts. Ingredients, design and cooking can complement one another; not every element has to be exceptional.

## Examples

### Choose between a few restaurants

> Use `$dinning` to compare these three restaurants. Food matters most to us, and our budget is ¥500 per person. Start with the one you would choose, then explain what informed your choice. Here are the restaurants and menus: …

### Examine an expensive menu

> Use `$dinning` to analyze this menu: do the ingredients justify the price, what stands out about the dish design, and how involved is the chef in the actual cooking? I've attached the menu and the chef's profile.

This fictional example shows the kind of response to expect:

**Input:** A restaurant costs ¥800 per person. Its menu lists “premium wagyu” without an origin or breed. The chef's profile says only “trained at renowned restaurants,” with no duration or role. A dining post contains plating photos and the word “amazing,” but no other assessment.

**Illustrative response:** With a food-first approach, I would pass on this restaurant. The expensive menu gives no specific information about the ingredients, the training claim says nothing about the chef's actual experience, and the recommendation does not explain what makes the food good. These materials do not support the restaurant's prices or positioning.

### Assess a dining recommendation

> Use `$dinning` to assess whether this recommendation is worth taking into account. Focus on whether it explains the ingredients, techniques and how the elements work together, and whether the reviewer has enough experience to make useful comparisons. Here are the recommendation and the reviewer's public information: …

The response starts with a recommendation, then explains the supporting details and gaps in the available information. Analysis based on photos is not presented as a firsthand tasting.

## FAQ

**Will it book a restaurant for me?** This skill handles selection and analysis, providing a judgment and the reasons behind it.

**Is it limited to one platform?** It can use restaurant websites, menus and public information across platforms, or analyze text and images you provide. Whether a page is accessible depends on the host agent's tools and access.

**What are its tastes?** Food comes first, with a strict view of investor-driven restaurant businesses, chains and standardized cooking. The rules also include preferences about specific areas and exceptions for individual brands. Read the full instructions in [SKILL.md](skills/dinning/SKILL.md).

**Which language are the docs and rules in?** This is the complete English introduction. The skill's instructions are maintained in a single Chinese `SKILL.md`.

## Files and validation

[skills/dinning/](skills/dinning/) is the installable skill, containing the complete instructions in [SKILL.md](skills/dinning/SKILL.md) and the Codex configuration in [agents/openai.yaml](skills/dinning/agents/openai.yaml). The repository-level `assets/` folder holds the README covers and design notes.

Skill format, rule consolidation, file links and README rendering have been checked. Its restaurant recommendations have not been validated against actual dining experiences.

## Contributing

Reports of ambiguous rules, outdated information and issues encountered in use are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for how to contribute.

## License and Lab 305

Licensed under [PolyForm Noncommercial 1.0.0](LICENSE), which permits noncommercial use, modification and distribution. Commercial use requires a separate license.

More from Lab 305: [LabKit](https://github.com/haorantang97/LabKit) · [Personal-Ontology](https://github.com/haorantang97/Personal-Ontology)
