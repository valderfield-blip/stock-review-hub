<div align="right">
  <a href="./README.md"><img alt="English" src="https://img.shields.io/badge/Language-English-0969DA"></a>
  <a href="./README.zh-CN.md"><img alt="简体中文" src="https://img.shields.io/badge/语言-简体中文-CB2431"></a>
</div>

# 美股复盘局

美股复盘局（Stock Review Hub）是一套 Codex Skill，用于生成面向专业投资者的中英双语美股每日复盘。它将经过验证的市场、宏观、财报、新闻、估值、情绪和量化数据整理为 HTML 报告，同时避免在公开页面中展示内部研究过程。工作流包含市场数据层、七位专业研究 Agent、投资委员会摘要和内容工作室，并持续维护可检索的每日档案、10 只个股跟踪池、多空逻辑、置信度、风险分析、回测指标及下一交易日观察事项。系统不会用虚构数值填补缺失数据：研究过程中缺失的信息会标记为 `DATA UNAVAILABLE`，无阅读价值的缺失字段不会在前台显示。

## 主要功能

- 固定使用七位研究 Agent，覆盖宏观、产业链、基本面、情绪、证据、风险和量化分析。
- 提供中英文双语报告结构，可作为静态 HTML 部署到 Vercel。
- 维护 10 只个股跟踪池，每只股票包含 Bull Case、Bear Case、Confidence Score 和跟踪备注。
- 提供日期搜索及 30 天、90 天、180 天历史复盘视图。
- 根据最新已核验复盘生成独立的口语化财经播客逐字稿，包含多空争议、深度评论和下一交易日观察；默认不在 HTML 中展示。
- 坚持证据优先，禁止虚构价格、涨跌幅、财务数据或平台情绪分数。

## 安装

克隆本仓库，并将 `stock-review-hub` 目录复制到 Codex skills 目录：

```bash
git clone https://github.com/valderfield-blip/stock-review-hub.git
cp -R stock-review-hub/stock-review-hub ~/.codex/skills/
```

安装后重启 Codex，使其识别新 Skill。

## 示例指令

```text
使用 $stock-review-hub 生成昨日的中英双语美股复盘，更新到历史记录顶部，维护 10 只个股跟踪池，并准备可部署至 Vercel 的 HTML 页面。
```

在线项目：[stock-review-hub.vercel.app](https://stock-review-hub.vercel.app)

本项目仅用于研究和教育，不构成投资建议。
