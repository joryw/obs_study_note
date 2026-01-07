Cloudflare Pages 主要用于托管静态/前端网站，并结合 Workers 打造「前端为主的全栈应用」，适合个人站点、文档、Landing Page 等场景。[1][2]

***

## Cloudflare Pages 是什么

- Cloudflare Pages 是一个面向前端开发者的 JAMstack 托管平台，可从 Git 仓库自动构建并部署静态或前端主导的应用。[1][3]
- 所有站点直接部署在 Cloudflare 全球边缘网络上，默认享受 CDN 加速、HTTPS 和 Cloudflare 其他安全能力。[1][2]

***

## 典型用途场景

- 个人主页、博客、作品集：利用静态站点生成器（如 Hugo、Hexo、Astro、Next 静态导出等）生成页面后自动部署，非常适合作为简历站和技术博客托管平台。[4][3]
- 产品官网、活动/营销页：快速搭建 Landing Page，通过 Git 提交即可上线/回滚，适合营销活动频繁更新的场景。[1][4]
- 文档站点、设计规范站：与 Git 仓库文档目录联动，每次合并 PR 自动更新文档，并为每个 PR 自动生成预览链接，方便团队评审。[1][5]
- Demo、实验项目：免费不限带宽与请求次数（在配额内），适合作为个人实验、开源项目 Demo、前端组件展示的托管方案。[2][6]

***

## 开发流程与协作用途

- CI/CD 自动化：连接 GitHub/GitLab/Bitbucket 后，每次 push 自动触发构建和部署，无需自搭 CI 服务。[4][3]
- 预览环境：每个提交或 Pull Request 都会生成独立预览 URL，方便产品、设计、QA 在线查看和反馈。[1][7]
- 团队协作：支持邀请团队成员共同管理项目，并提供访问控制、预览保护（结合 Cloudflare Access 做登录保护）。[1][2]

***

## 与 Workers / 后端的组合用途

- 全栈/边缘应用：Pages 前端 + Workers/Functions 做 API/动态逻辑，实现认证、表单处理、A/B 测试、重写/重定向等功能。[1][4]
- 数据与存储：结合 D1（数据库）、KV、R2 等产品，可以构建评论系统、计数器、小型业务后台等「无服务器」应用。[4][3]
- 定时任务与后台任务：利用 Pages Functions/Workers 的 Cron、后台任务处理周期性数据、同步第三方 API 等。[4]

***

## 运维与成本方面的用途

- 降低运维成本：无需自建 Web 服务器、CDN 或 SSL，所有构建与部署在 Cloudflare 平台内完成。[1][4]
- 回滚与安全：提供原子化部署与一键回滚，减少上线风险，默认自动签发 HTTPS 证书，避免证书过期问题。[2][4]
- 指标与分析：内置隐私友好的 Web Analytics，可直接查看访问量、性能指标，而不依赖前端埋点脚本（更不易被广告拦截）。[1][4]

如果你告诉目前打算放什么类型的网站（博客、项目文档、Landing Page、还是小应用），可以再帮你写一小段「按场景」的 Pages 使用笔记。

Sources
[1] Pages | Full-stack platform for frontend developers - Cloudflare https://www.cloudflare.com/developer-platform/products/pages/
[2] Cloudflare Pages https://pages.cloudflare.com
[3] Overview · Cloudflare Pages docs https://developers.cloudflare.com/pages/
[4] What is Cloudflare Pages: A Review of Deployment Features https://bejamas.com/hub/hosting/cloudflare-pages
[5] Introducing Cloudflare Pages: the best way to build JAMstack websites https://blog.cloudflare.com/cloudflare-pages/
[6] Cloudflare Pages - small website https://www.reddit.com/r/CloudFlare/comments/16f1q87/cloudflare_pages_small_website/
[7] Cloudflare launches Cloudflare Pages, a platform to deploy and host ... https://techcrunch.com/2020/12/17/cloudflare-launches-cloudflare-pages-a-platform-to-deploy-and-host-jamstack-sites/
[8] Is there any benefit to hosting on Cloudflare Pages over hosting on GitHub Pages with Cloudflare in front of it? https://www.reddit.com/r/CloudFlare/comments/1jj6lex/is_there_any_benefit_to_hosting_on_cloudflare/
[9] Cloudflare Pages: Best server tech since CGI-bin? https://news.ycombinator.com/item?id=33307950
[10] Introducing Cloudflare Pages: the best way to build JAMstack websites https://www.reddit.com/r/webdev/comments/key06w/introducing_cloudflare_pages_the_best_way_to/
[11] Is Cloudflare Pages the right choice for my project? https://www.reddit.com/r/webdev/comments/1c5hhj4/is_cloudflare_pages_the_right_choice_for_my/
[12] Cloudflare Pages (free features) https://www.reddit.com/r/CloudFlare/comments/1f1oayo/cloudflare_pages_free_features/
[13] Cloudflare Pages: Build a Static Website in Minutes (Free) https://www.youtube.com/watch?v=mzNpuj4T66Q
[14] Anyone tried Cloudflare Pages? https://www.reddit.com/r/softwaredevelopment/comments/kyeicu/anyone_tried_cloudflare_pages/
[15] Deploy your Website for free Cloudflare Pages https://www.youtube.com/watch?v=k7fUkTQvCzk
[16] Cloudflare Pages - Zola https://www.getzola.org/documentation/deployment/cloudflare-pages/
[17] Cloudflare Pages is shockingly good and nobody talks about it? https://www.reddit.com/r/statichosting/comments/1nw0ln9/cloudflare_pages_is_shockingly_good_and_nobody/
[18] Cloudflare Pages free forever. What's the catch? https://www.reddit.com/r/CloudFlare/comments/16fjh45/cloudflare_pages_free_forever_whats_the_catch/
[19] CloudFlare Pages https://www.reddit.com/r/selfhosted/comments/1bwzpms/cloudflare_pages/
[20] Workers vs Pages https://www.reddit.com/r/CloudFlare/comments/1ip87mx/workers_vs_pages/

Cloudflare 主要用来提升网站的**性能**、安全和可用性，可以当作「网站前面的一层保护和加速网」。[1][2]

下面是一份适合做笔记、以后回顾用的整理，你可以直接复制到自己的文档里。

***

## Cloudflare 是什么

- Cloudflare 是一个位于用户和源站服务器之间的反向代理网络服务，用于加速和保护网站、API 和应用。[1][3]
- 它提供 CDN、DDoS 防护、WAF、防火墙、DNS、Zero Trust、边缘计算等一整套服务。[2][4]

***

## 核心用途概览

- 提升访问速度：通过全球 CDN 节点缓存静态内容、智能路由、压缩和图片优化等手段降低延迟。[2][5]
- 提高安全性：提供 DDoS 防护、WAF、Bot 管理、SSL/TLS 加密和隐藏源站 IP。[6][7]
- 增强可用性：负载均衡、健康检查和 Anycast 网络，帮助网站在单点故障时继续对外提供服务。[2][8]
- 简化运维：集中做 DNS 管理、证书管理、访问控制和日志分析，降低日常维护成本。[9][4]

***

## 性能相关用途

- CDN 加速：将静态资源缓存到全球 300+ 数据中心，就近回源，减少跨区域访问延迟。[2][7]
- 智能路由：Argo Smart Routing 挑选更快、拥塞更少的网络路径，降低首字节时间。[2]
- 前端优化：如 Rocket Loader（优化 JS 加载）、图片压缩（Polish）、图片加载优化（Mirage）、Brotli 压缩等。[2][5]

***

## 安全相关用途

- DDoS 防护：在边缘节点吸收和过滤大流量攻击，避免源站被打挂。[2][5]
- Web 应用防火墙（WAF）：拦截 SQL 注入、XSS 等常见 Web 攻击，支持自定义规则和托管规则集。[6][10]
- Bot 管理：识别并拦截恶意爬虫、撞库、刷接口等行为，保护业务接口和资源。[6][4]
- SSL/TLS 加密：自动申请和续期证书，强制 HTTPS，降低证书运维成本并提升数据传输安全。[6][4]
- Zero Trust 访问：通过身份验证、设备检查等方式保护内部系统访问（Cloudflare Access、Gateway 等）。[2][11]

***

## DNS 与网络用途

- DNS 托管：托管域名 DNS 记录，提供快速的解析和 DNSSEC 等安全能力。[9][2]
- 反向代理：隐藏源站 IP，统一在 Cloudflare 这一层做缓存、加密和访问控制。[6][3]
- 负载均衡：在多台源服务器之间分发流量，并根据健康检查把流量导向可用节点。[2][8]
- 企业网络：通过 Magic Transit、WAN-as-a-Service 等，替代传统 VPN/专线构建企业广域网。[2][11]

***

## 开发与边缘计算用途

- Cloudflare Workers：在边缘运行无服务器代码（JS/TS 等），做重定向、A/B 测试、API 网关、定制逻辑等。[6][2]
- KV / Durable Objects：分布式 KV 存储和有状态对象，用于会话、计数器、房间状态等应用场景。[2]
- Pages & R2：静态网站托管（Pages）和 S3 兼容对象存储（R2），适合部署前端站点和静态资源。[2][12]

***

## 典型使用场景（可以按需勾选）

- 给公开网站加速 + 防护：中小网站接入 Cloudflare 免费/Pro 计划，用 CDN + WAF + DDoS 防御。[8][13]
- 保护遗留/脆弱站点：在不改动代码的情况下，用 WAF 和规则给老系统加一层“安全外壳”。[8]
- 自建服务暴露到公网：用 Cloudflare Tunnel 把内网服务安全暴露给外部访问，无需直接开放端口。[2]
- 多节点业务：多机房、多云部署时，用其负载均衡与健康检查做流量调度和故障切换。[2][11]

***

如果你愿意，可以说说你现在打算怎么用 Cloudflare（比如：只做 DNS + CDN，还是要用 Workers/Zero Trust），可以帮你把这份笔记再改成更针对你场景的版本。

Sources
[1] What is Cloudflare? https://www.cloudflare.com/learning/what-is-cloudflare/
[2] Understanding Cloudflare: Features, Services & How It Works https://www.newpathweb.com.au/blog/understanding-cloudflare-how-it-works-features-and-services/
[3] Cloudflare - Wikipedia https://en.wikipedia.org/wiki/Cloudflare
[4] Cloudflare Explained: Features, Benefits, and How to Use It for Your Website - HostScore https://hostscore.net/learn/cloudflare/
[5] Top 15+ Cloudflare Benefits for Enhanced Web Performance https://cyberpanel.net/blog/cloudflare-benefits
[6] What is Cloudflare | How it Works and When do you use it? https://www.geeksforgeeks.org/computer-networks/what-is-cloudflare/
[7] Cloudflare services overview - Dalaric Ltd https://dalaric.com/kb/cloudflare-services-overview/
[8] What is your primary use case for Cloudflare? https://www.peerspot.com/questions/what-is-your-primary-use-case-for-cloudflare
[9] Features and plans · Cloudflare DNS docs https://developers.cloudflare.com/dns/reference/all-features/
[10] Common use cases for custom rules https://developers.cloudflare.com/waf/custom-rules/use-cases/
[11] Network Services Product Offerings https://www.cloudflare.com/network-services/products/
[12] What is Cloudflare and when do you use it? https://www.reddit.com/r/webdev/comments/wwyh5g/what_is_cloudflare_and_when_do_you_use_it/
[13] Cloudflare Pricing Guide for Security Products https://underdefense.com/industry-pricings/cloudflare-ultimate-guide-for-security-products/
[14] Cloudflare: A Complete Guide, Features & Walkthrough https://www.youtube.com/watch?v=BlhbsHrmcDc
[15] Use cases https://developers.cloudflare.com/use-cases/
[16] Use Cases of Cloudflare 2025 https://www.trustradius.com/products/cloudflare/reviews?qs=product-usage
[17] What is Cloudflare? Features, Benefits, and How It Works https://www.theknowledgeacademy.com/blog/what-is-cloudflare/
[18] Why are so many people here using Cloudflare? Aren't you guys selfhosters for a reason? I think everybody here is trying to get away from big world-controlling companies.. https://www.reddit.com/r/selfhosted/comments/v18gk7/why_are_so_many_people_here_using_cloudflare/
[19] [PDF] Cloudflare Product Cheat Sheet.pptx https://www.cloudflare.com/static/6f129010d43216d460e308819acce421/Cloudflare_Product_Cheat_Sheet.pptx.pdf
[20] Cloudflare Features 2025 - TopAdvisor https://www.topadvisor.com/products/cloudflare/features
