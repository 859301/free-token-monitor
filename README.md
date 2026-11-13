# 免费 Token 监控平台

给 Agent 的免费口粮：聚合全网经厂商官方页核对过的免费额度，帮你把每天、每周、每月能领的免费 Token 一次看完，优先选能直接接进 Agent 的 API 额度。

> 数据仅供参考，以厂商官方页为准。额度随时可能调整或结束；领取前请看清对方条款。

## 在架数据

- 共 43 条（生成于 2026-11-09），覆盖大模型、编程、搜索、算力、浏览器、数据、语音七类。
- 数据来源：蓝蓝仓库、freetokens.fyi，均经厂商官方页核对。
- 每条数据只照录官方原文，不做自创人民币折算。额度原文、领取链接、门槛、风险、领取步骤、核实日期都在 `data/offers.json` 里。
- 本站不含邀请链接、API 中转站、二手积分、共享账号、接码多开等内容。

## 免费 VPS 板块

- 共 10 条（8 条核实于 2026-11-12，InstaBox 与 EUserv 核实于 2026-11-13），分五组：永久免费 2 条（甲骨文、Google Cloud）、试用/额度 5 条（AWS、Azure、阿里云、腾讯云、Kamatera）、学生专属 1 条（Azure for Students）、免费沙箱 1 条（InstaBox，非传统 VPS）、免费但需手动续期 1 条（EUserv VS2-free，IPv6-only）。
- 数据在 `data/vps.json` 里，字段与 `data/offers.json` 对应（另有 `group`、`specText`、`durationText`、`cardNote`、`flags`、`notes` 字段；`cardRequired` 为 `null` 表示官方页未说明；`group` 新增 `manual-renew`，表示免费但需手动续期）。
- 板块页面在 `vps/` 下：列表页、10 篇详情页、8 篇对比、4 篇指南、1 个问答页（20 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- 未收录说明：华为云（状态未核实）、Vultr / DigitalOcean（说法矛盾）、任务续费型主机、退款保证类「试用」等暂不收录，原因写在 `vps/index.html` 的「未收录及原因」一节。试用额度与任务主机现已在羊毛板块按羊毛规则收录，见下「羊毛 VPS 板块」一节。

## 免费虚拟主机板块

- 共 11 条（核实于 2026-11-13）：10 家免费虚拟主机（8 家参数较完整、2 家部分信息未确认）+ 000webhost 已停服档案。
- 数据在 `data/hosting.json` 里，字段与 `data/vps.json` 对应（另有 `disk`、`bandwidth`、`databases`、`php`、`ssl`、`ads`、`idlePolicy`、`panel`、`installer` 字段；`group` 取值：`verified` / `conditional` / `archive`；`status` 取值：`active` / `conditional` / `dead`；`cardRequired` 为 `null` 表示官方页未说明）。
- 板块页面在 `hosting/` 下：列表页、11 篇详情页与档案页、5 篇对比、6 篇指南、1 个问答页（18 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- EUserv VS2-free 是 VPS 形态，归在免费 VPS 板块（`group` 为 `manual-renew`），续期任务属性在羊毛板块说明。

## 羊毛 VPS 板块

- 共 7 条（6 条在架 + 1 个历史档案；核实于 2026-11-12/13），分三组：试用额度 4 条（Vultr、Hetzner、Akamai、DigitalOcean）、任务续费主机 1 条（三丰云，仅规格已核实）、沙箱额度 1 条（Simular Box，条款说法冲突）；另有 RackNerd 黑五历史档案与搬瓦工优惠码核查笔记。
- 数据在 `data/wool.json` 里，字段与 `data/vps.json` 对应（另有 `priceText`、`validityText`、`riskLevel`、`renewalText`、`taskBurden`、`codeRequired` 字段；`status` 取值含 `disputed` 与 `historical`）。
- 板块页面在 `wool/` 下：列表页、8 篇详情页与核查笔记、3 篇对比、5 篇指南、1 个问答页（12 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- 标签规则：风险等级（低/中/高）、有效期、续费条件、任务负担、优惠码依赖逐条写明；本站不刊登优惠码字符串。

## 低价 VPS 板块

- 共 4 条（核实于 2026-11-13）：常态价 3 家（RackNerd、HostEONS、DigitalOcean）+ 缺货观察 1 个（Hetzner CX23，非在售）。
- 数据在 `data/cheap.json` 里，字段与 `data/vps.json` 对应（另有 `priceText`、`validityText`、`riskLevel`、`renewalText`、`renewalStatus`、`plans` 字段；`renewalStatus` 取值：`stated-same-rate` / `list-price` / `unknown`）。
- 板块页面在 `cheap/` 下：列表页、4 篇详情页与缺货观察、4 篇对比、6 篇指南、1 个问答页（10 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- 边界规则：只收常态价（常态套餐页 + 无截止日期 + 续费条件写明或为目录价）；限时促销、首期价与优惠码价一律归羊毛板块。

## 部署与托管板块

- 共 10 条（核实于 2026-11-13）：7 个免费层（Vercel、Netlify、Cloudflare Workers、Cloudflare Pages、Render、Northflank、EdgeOne）+ 1 个试用（Railway，30 天 $5 credits）+ 2 个无免费层说明（Fly.io、Koyeb）。
- 数据在 `data/deploy.json` 里，字段与 `data/hosting.json` 对应（另有 `planKind`、`hostingType`、`limitsText`、`overageBehavior`、`sleepPolicy`、`commercialNote`、`paidFrom` 字段；`group` / `status` 取值：`free` / `trial` / `no-free-tier`；`cardRequired` 为 `null` 表示官方页未说明；无 `steps` 字段，证据中没有各家的注册流程）。
- 板块页面在 `deploy/` 下：列表页、10 篇详情页、5 篇对比、6 篇指南、1 个问答页（17 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- GitHub Pages（参数未直接核实）与 Heroku 免费 tier（已于 2022-11-28 移除）只在列表页「不在列表中的服务及原因」一节说明。

## 免费数据库板块

- 共 6 条（核实于 2026-11-13）：Supabase、Neon、Turso、Upstash Redis、MongoDB Atlas M0、Firebase（Firestore/Auth/Hosting，Hosting 不另建详情页）。
- 数据在 `data/database.json` 里，字段与 `data/hosting.json` 对应（另有 `dbType`、`overage`、`upgrade`、`idlePolicy`、`storage`、`freePlan` 字段；`group` 取值：`verified`；`status` 取值：`active`；`cardRequired` 为 `null` 表示官方页未说明）。
- 板块页面在 `database/` 下：列表页、6 篇详情页、5 篇对比、6 篇指南、1 个问答页（16 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- PlanetScale Hobby（已于 2024-04-08 退役）只在列表页「不在列表中的服务及原因」一节说明。

## 域名 / DNS / CDN / SSL 板块

- 共 6 条（核实于 2026-11-13）：Cloudflare 免费计划、Let's Encrypt、is-a.dev（部分信息未确认）与 3 家低价注册商（Porkbun、Namecheap、Spaceship，首年价与续费价分开列出）。
- 数据在 `data/domain.json` 里，字段与 `data/hosting.json` 对应（另有 `serviceType`、`priceText`、`keyLimits`、`firstYear`、`renewal`、`transfer`、`icannFee`、`privacy` 字段；`group` 取值：`verified` / `conditional` / `low-price`；`status` 取值：`active` / `conditional`；`cardRequired` 为 `null` 表示官方页未说明）。
- 板块页面在 `domain/` 下：列表页、6 篇详情页、5 篇对比、6 篇指南、1 个问答页（16 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- Freenom 免费域名（已死）、eu.org / JS.ORG / DigitalPlat（官网条款未确认）只在列表页「不在列表中的服务及原因」一节说明；GitHub Student Pack 域名优惠只作交叉提示。

## 邮件通知板块

- 共 5 条（核实于 2026-11-13）：3 个免费层（Resend、Brevo、Postmark）+ 1 个官网未明示永久（Mailgun）+ 1 个试用（SendGrid，60 天）。
- 数据在 `data/email.json` 里，字段与 `data/hosting.json` 对应（另有 `planKind`、`planName`、`limitKind`、`limitsText`、`overageBehavior`、`paidFrom` 字段；`group` / `status` 取值：`free` / `not-stated-permanent` / `trial`；`cardRequired` 为 `null` 表示官方页未说明；SendGrid 的 PDF 与网页超额费率并列记录）。
- 板块页面在 `email/` 下：列表页、5 篇详情页、4 篇对比、5 篇指南、1 个问答页（15 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- SendGrid 永久免费计划（已于 2025 年 3–5 月退役）只在列表页「不在列表中的服务及原因」一节说明，并链向已死服务指南。

## 监控分析板块

- 共 7 条（核实于 2026-11-13）：6 个免费层（UptimeRobot、Sentry、Umami、PostHog、Clarity、Google Analytics 4）+ 1 个试用（Plausible，30 天）。
- 数据在 `data/monitoring.json` 里，字段与 `data/hosting.json` 对应（另有 `planKind`、`planName`、`monitoringType`、`retentionText`、`limitsText`、`overageBehavior`、`paidFrom` 字段；`group` 取值：`free` / `trial`；`status` 取值：`active` / `trial`；`cardRequired` 为 `null` 表示官方页未说明；Sentry 的 5k/5M/50 三项数字不带周期表述；UptimeRobot 的卡片与对比表冲突记在 `notes` 里）。
- 板块页面在 `monitoring/` 下：列表页、7 篇详情页、5 篇对比、5 篇指南、1 个问答页（16 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- 自托管监控软件（Uptime Kuma、UptimeFlare 等）只在指南中说明，不列入列表。

## 支付变现板块

- 共 4 条（核实于 2026-11-13）：1 个支付处理（Stripe）+ 3 个 Merchant of Record（Paddle、Lemon Squeezy、Polar）。
- 数据在 `data/payments.json` 里，字段与 `data/hosting.json` 对应（另有 `feeText`、`monthlyFee`、`morStatus` 字段；`group` 取值：`processor` / `merchant-of-record`；`status` 取值：`active`；`cardRequired` 为 `null` 表示官方页未说明）。
- 板块页面在 `payments/` 下：列表页、4 篇详情页、4 篇对比、5 篇指南、1 个问答页（18 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- 灰色渠道（买卖/代办账户）只在列表页与大陆个人收款指南中作一行风险提示，不作任何操作说明；Lemon Squeezy 迁移后费率不写沿用旧费率的说法。

## 认证板块

- 共 2 条独立认证（核实于 2026-11-13）：Clerk、Auth0；Supabase Auth 与 Firebase Auth 随数据库免费档提供，只作交叉指引，不重复列出。
- 数据在 `data/auth.json` 里，字段与 `data/hosting.json` 对应（另有 `planName`、`limitsText`、`overageBehavior` 字段；`group` 取值：`standalone`；`status` 取值：`active`；`cardRequired` 为 `null` 表示官方页未说明）。
- 板块页面在 `auth/` 下：列表页、2 篇详情页、3 篇对比、4 篇指南、1 个问答页（14 问），均已加入 `sitemap.xml` 与 `llms.txt`。

## 对象存储板块

- 共 2 条（核实于 2026-11-13）：1 个免费层（Cloudflare R2）+ 1 个按量付费（Backblaze B2，无免费层）；Supabase Storage 与 Firebase Storage 只作交叉指引，不重复列出。
- 数据在 `data/storage.json` 里，字段与 `data/hosting.json` 对应（另有 `limitsText`、`overageBehavior`、`egressText` 字段；`group` / `status` 取值：`free` / `pay-as-you-go`；`cardRequired` 为 `null` 表示官方页未说明）。
- 板块页面在 `storage/` 下：列表页、2 篇详情页、4 篇对比、3 篇指南、1 个问答页（14 问），均已加入 `sitemap.xml` 与 `llms.txt`。

## 代码托管板块

- 共 2 条（核实于 2026-11-13）：GitHub Free、GitLab Free。
- 数据在 `data/code.json` 里，字段与 `data/hosting.json` 对应（另有 `planKind`、`planName`、`limitsText` 字段；`group` 取值：`free`；`status` 取值：`active`；`cardRequired` 为 `null` 表示官方页未说明，为 `false` 表示官网写明无需信用卡）。
- 板块页面在 `code/` 下：列表页、2 篇详情页、3 篇对比、4 篇指南、1 个问答页（15 问），均已加入 `sitemap.xml` 与 `llms.txt`。
- 已死服务指南在 `guides/dead-services/` 下：Heroku、PlanetScale、SendGrid 永久免费计划、Freenom、Upstash Kafka、Google Domains 的现状与替代，时间线来自多家公开报道。

## 工作流总览

- 工作流总览页在 `workflow/` 下：14 个环节的阶段地图、从零上线检查清单与 3 套 $0 组合，已加入 `sitemap.xml` 与 `llms.txt`。
- 方法论指南在 `guides/` 下新增 3 篇：`idea-validation`（立项验证）、`peripheral-capabilities`（周边能力）、`launch-operations`（上线运营），均为概念与检查清单，不含厂商参数。

## 使用方法

### 本地打开

直接双击 `index.html` 即可打开页面。但部分浏览器会拦截本地文件读取 `data/offers.json`，打不开数据时页面会提示；这时用本地服务器打开：

```bash
python3 -m http.server 8000
```

再访问 http://localhost:8000/

### GitHub Pages

仓库推送后按 `.github/workflows/pages.yml` 自动部署到 GitHub Pages，打开仓库的 Pages 地址即可使用，无需构建步骤。

## 筛选与台账

页面顶部显示今日可领、每日口粮条数、7 天内到期、今日已领和连续领取天数。

筛选器：

- 搜索框：按标题和厂商搜索
- 分类：大模型 / 编程 / 搜索 / 算力 / 浏览器 / 数据 / 语音
- 节奏：每天 / 每周 / 每月 / 一次 / 长期
- 只看 API 直调：只显示能直接调 API 的额度，排除只能在客户端里用的
- 免绑卡：排除要求绑定支付方式的
- 国内直连：只显示国内可直连的
- 只看未领：隐藏本周期已标记的
- 排序：按到期时间 / 按核实时间

每张卡显示厂商、标题、额度原文、接入方式、是否 OpenAI 兼容、门槛、风险、领取步骤、核实日期、到期倒计时，点「去领取」在新标签打开厂商官方页。

领取台账：

- 点「标记已领」记录一次领取，点「已领（点撤销）」可撤销（手滑点错用）。
- 台账只保存在本浏览器（localStorage），按北京时间日 / 周 / 月自动翻篇：每天的次日 0 点、每周的周一、每月的 1 日重新变为未领；一次性和长期额度领过即记为已领。
- 连续天数按每天至少领过一次来算，换浏览器或清理网站数据会重置。

## 数据更新方式

1. 对照厂商官方页逐条核对 `data/offers.json`：额度、链接、截止时间、门槛有变化就改对应字段，`verifiedAt` 改成核对当天。
2. 到期的条目把 `status` 改成 `expired`（或直接删除），不要留着误导人。
3. 新活动先核对官方页再加一条，`slug` 全站唯一，`claimUrl` 必须是厂商官方页，不要放邀请链接和中转站。
4. 改完后本地打开页面确认能正常加载，提交并推送，GitHub Pages 会自动重新部署。

## 免责声明

- 本项目只做公开信息的聚合与整理，不提供任何账号、密钥、中转服务。
- 所有额度以厂商官方页为准，随时可能调整、提前结束或被领完；页面上的核实日期只说明最后一次核对的时间。
- 部分免费额度用完后可能默认转按量计费，请在厂商控制台开启「用完即停」或同类开关，避免意外扣费。
- 请遵守各厂商的使用条款，不要用多开、共享账号等违规方式领取。

## 许可证

MIT License，见 [LICENSE](LICENSE)。

## 英文版（English edition）

- 英文页在 `en/` 下（首批，2026-11-13）：24 页——4 个板块列表页、10 篇详情页、6 篇对比、1 个综合问答页（23 问）、3 个 Hub 页。
- 英文数据文件 `data/offers-en.json`、`data/vps-en.json`、`data/wool-en.json`、`data/cheap-en.json`：文本译为英文，事实（金额、日期、条款、规格、链接、核实日期）与中文数据文件完全一致；中文数据文件是事实来源，不要单独改 `-en` 文件里的事实字段。
- 每篇英文页都在 `<head>` 里用 hreflang 指向中文对应页（`en` / `zh-CN` / `x-default`），中文为默认语言；中文对应页也加了回链。英文列表页为静态页，不含领取台账（无 localStorage）。
