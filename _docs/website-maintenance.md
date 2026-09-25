# 网站更新指南

网站继续通过 GitHub Pages 发布。日常更新只改数据文件，不需要调整页面排版。

## 1. 新增论文：只录入一次

在 `_data/publications.yml` 相应年份的位置添加记录。文件内顺序决定同一年论文的显示顺序；年份自动从新到旧排列。

```yaml
- id: project-paper-2027
  project_id: project-name
  title: Full Paper Title
  short_title: Short Project Name
  authors:
  - First Author
  - Bo Liu
  - Last Author
  year: 2027
  venue: CHI
  type: Conference paper
  doi: 10.xxxx/xxxx
```

`id` 必须唯一；`project_id` 与 projects.yml 中的项目对应。`authors` 按正式论文排序。模板自动加粗 Bo Liu，并根据作者顺序显示 First author 或 Co-author；它不会推测具体个人贡献。

同一项目的主论文、demo 使用相同 `project_id`，但各自有独立论文 `id` 和 DOI。它们在 Publications 分别列出，在 Research 共用一张卡片。`type: Demo` 会显示为 Demo paper 链接。可选 `preprint` 用于预印本网址。 设置 `show_on_project: false` 可隐藏该论文在 Research 项目卡片中的链接，Publications 和 News 中的记录不受影响。

## 2. 新增或更换精选项目

在 `_data/projects.yml` 添加项目，设置 `featured: true`。按文件顺序展示，建议保留 4–6 项。

```yaml
- id: project-name
  name: Project Name
  featured: true
  topic: Sensing · Interaction
  image: /images/research/project-name.webp
  image_alt: An accurate description of the image
  summary: Two short sentences about the research.
  contribution: My confirmed responsibilities.
  url: https://example.org/project/
  video: https://www.youtube.com/watch?v=example
```

`contribution`、`url` 和 `video` 都可省略。只写已确认的个人职责。已有实验室或作者项目页时，用 `url` 直接链接，无需另建详情页。没有独立项目页时，卡片标题链接到第一篇关联论文。

图片放进 `images/research/`，保持内容完整，建议宽度约 1200 px、体积低于 150 KB。为图片填写准确的替代文字。图片来源记录在 `_docs/research-image-sources.md`。

只出现在论文列表中的项目设置 `featured: false`；它不需要图片和摘要。精选项目至少要有一条关联论文，首条关联论文决定卡片的会议年份和作者身份。

## 3. 只为重要进展添加新闻

在 `_data/news.yml` 顶部添加记录。最近 3 条默认展开，其余自动放入 Earlier updates。

```yaml
- date: Apr 2027
  lead: "Published:"
  publication_ids: [project-paper-2027]
```

标题、会议、年份、DOI 都从论文数据读取，不要在这里重复维护。`Accepted:` 用实际录用月份；`Published:` 用正式发表月份，二者不要混用。只有重要进展需要添加新闻，新论文不会自动成为新闻。

不关联论文的事件可用 `date`、`text` 和可选 `url`。此前历史新闻仍保存在这个文件中。

## 4. 原有详细项目页

`/portfolio/Lulaland/` 和 `/portfolio/SmartRecorder/` 保持可访问。它们使用 front matter 中的 `project_id`，通过 `project-publications.html` 自动显示论文作者、会议、链接及已确认贡献，不再手工复制。

其他早期项目保留在 Research 的 Earlier projects 中。CV PDF 仍单独维护，不会由这次论文数据自动生成。

## 发布与检查

将变更提交并推送到 `master`，GitHub Pages 会自动构建。确认 Actions 的 pages-build-deployment 成功，再打开 Research、Publications 和首页检查。无需操作 Northwest、WordPress 或 DNS。

普通内容更新不需要修改 `_includes/` 或 `_sass/` 中的模板和样式文件。
