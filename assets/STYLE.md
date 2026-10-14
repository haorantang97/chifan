# Visual direction

## Identity

- Repository: `restaurant-screening`
- Chinese name: 餐厅筛选与避雷
- Purpose: food-first restaurant screening through 经营模式、菜肴品质、人的经验.
- One Skill, with three parallel areas of judgment.

## Reference and motif

Original editorial direction; no external visual reference was supplied. An engraved plate with simple ingredient forms and four observation corners expresses looking closely at the food. The three areas appear together in one line, without numbered stages or progress arrows.

## Palette

| Role | Light | Dark |
| --- | --- | --- |
| Background | `#F6F3E9` | `#17231C` |
| Title | `#253D2E` | `#F0F1E3` |
| Secondary text | `#61715E` | `#B6C3AC` |
| Plate | `#E7EBD9` | `#24362A` |
| Accent | `#B74F32` | `#EE9471` |

## Typography and dimensions

Native SVG text uses PingFang SC, Hiragino Sans GB, Microsoft YaHei and Noto Sans CJK SC, with a sans-serif fallback. The Chinese title is primary at 74 px; the repository slug is secondary. Both heroes use a `1000 × 320` viewBox. At 320 px wide, the title remains approximately 24 px tall. Do not add small operational copy to the hero.

## Files and usage

- `hero.svg`: light background.
- `hero-dark.svg`: dark background.

Embed with a `picture` element that selects `hero-dark.svg` for `prefers-color-scheme: dark` and uses `hero.svg` as the `img` fallback. Provide a descriptive Chinese alt text and display at full available README width, up to 1000 px. Both files include a title, description and responsive viewBox.

The artwork uses Chinese text and the shared repository slug. It is not a separately configured social preview.
