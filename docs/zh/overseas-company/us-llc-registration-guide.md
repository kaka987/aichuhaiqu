---
title: "美国 LLC 注册全流程：从选州到拿 EIN"
code: "A02"
description: "手把手走一遍美国 LLC 注册流程。选州（Wyoming/Delaware/New Mexico）、注册代理、Articles of Organization、EIN 申请、银行开户，每一步的费用、时间和注意事项。"
date: 2026-06-24
tags: [overseas-company]
---

# 美国 LLC 注册全流程：从选州到拿 EIN

注册美国 LLC 这件事，没有想象中复杂，但里面有几个容易踩的坑。这篇按照实际操作顺序，把每一步拆开讲清楚。

## 第一步：选州

美国有 50 个州，每个州都可以注册 LLC。但对中国开发者来说，常见选择就三个：

| 州 | 注册费 | 年审费 | 优势 | 劣势 |
|----|--------|--------|------|------|
| Wyoming | $100 | $60/年（年报费） | 无州所得税、无 Franchise Tax、隐私保护强（不公开成员信息）、注册代理便宜 | 知名度略低于 Delaware |
| Delaware | $90 | $300/年（Franchise Tax） | 商业法律体系成熟、投资人认可度高 | 年维护成本高、单人 LLC 没有必要选这里 |
| New Mexico | $50 | $0（无年报要求） | 最便宜、无年报、隐私好 | 部分银行和平台对 NM LLC 接受度略低 |

**对独立开发者的建议：选 Wyoming。** 理由很简单——年维护成本低（$60 vs Delaware 的 $300）、隐私保护好、主流银行和支付平台（Stripe、Mercury、Wise）全部支持。除非你打算融资（投资人偏好 Delaware C-Corp），否则 Wyoming LLC 是性价比最高的选择。

New Mexico 看起来更便宜（$0 年审），但实际操作中，有些银行会对 NM LLC 多问几个问题，开户体验不如 Wyoming 顺畅。省下的钱不多，增加的摩擦不值得。

## 第二步：选注册代理（Registered Agent）

美国法律要求每个 LLC 必须有一个在注册州有实际地址的 Registered Agent，用来接收政府文件和法律通知。你人在中国，显然不能自己当。

需要找一家注册代理服务商。常见选择：

| 服务商 | 年费 | 说明 |
|--------|------|------|
| Northwest Registered Agent | $125/年 | 老牌，口碑好，首年注册 LLC 含注册代理服务 |
| Registered Agents Inc. | $99/年 | 价格低，服务稳定 |
| Wyoming Agents | $25-50/年 | 本地小型代理，便宜但服务响应慢 |
| Firstbase.io | $399/年（含注册） | 一站式打包（注册+EIN+银行开户指导），适合不想折腾的人 |
| Stripe Atlas | $500 一次性 | Stripe 官方服务，注册 LLC + EIN + Stripe 账号 + Mercury 银行账号一条龙 |

**怎么选：**

- 预算紧 + 愿意自己跑流程 → Northwest 或 Registered Agents Inc.
- 不想折腾、愿意多花钱买省心 → Stripe Atlas（$500 全搞定，而且 Stripe 账号自动就有了）
- 已经注册过 LLC、只需要换代理 → 选最便宜的就行

Stripe Atlas 的 $500 包含：Wyoming/Delaware LLC 注册 + EIN + Stripe 账号 + Mercury 银行账号开户 + Operating Agreement 模板 + 一年注册代理。对于目标明确就是要用 Stripe 收款的开发者，这是最省心的路径。

## 第三步：提交注册文件（Articles of Organization）

选好州和注册代理后，需要向州务卿办公室（Secretary of State）提交 Articles of Organization。这是一份很简单的文件，核心信息就几项：

- LLC 名称（不能和已有公司重名，提前在州务卿网站查询）
- 注册代理名称和地址
- LLC 的用途（通常填 "any lawful purpose"）
- 管理结构（Member-managed 还是 Manager-managed，单人选 Member-managed）
- 组织者（Organizer）信息

**如果你用注册代理服务商注册：** 他们会帮你填表、提交、跟踪进度。你只需要提供 LLC 名称和你的联系方式。

**如果你自己注册（Wyoming 为例）：**
1. 去 Wyoming Secretary of State 官网：https://sos.wyo.gov
2. 在线填写 Articles of Organization
3. 支付 $100 注册费（信用卡）
4. 等待审批（通常 1-3 个工作日）

Wyoming 的效率很高，网上提交后 1-3 天就能批下来。Delaware 也很快，1-2 天。批准后你会收到一份 Certificate of Organization（相当于营业执照）。

## 第四步：准备 Operating Agreement

Operating Agreement 是 LLC 的内部运营协议，规定成员权益、利润分配、管理方式等。单人 LLC 也需要这份文件——不是法律强制要求（各州不同），但银行开户和 Stripe 注册时可能会要。

如果你用 Stripe Atlas 或 Firstbase，他们会给你一份标准模板。自己注册的话，网上搜 "Single Member LLC Operating Agreement template" 有大量免费模板，改一下公司名和成员名就行。

关键条款：
- 你是唯一 Member，持有 100% 权益
- Member-managed 结构
- 利润全部分配给唯一 Member
- 解散条款

这份文件不需要提交给州政府，自己保存好就行。

## 第五步：申请 EIN（雇主识别号）

EIN 是美国国税局（IRS）分配给公司的税务识别号，相当于公司的「身份证号码」。开银行账户、注册 Stripe、报税都需要它。

**申请方式：**

| 方式 | 费用 | 时间 | 适用情况 |
|------|------|------|---------|
| IRS 官网在线申请 | 免费 | 即时（但需要 SSN/ITIN） | 有 SSN 或 ITIN 的人 |
| IRS 传真/邮寄 SS-4 表格 | 免费 | 传真 4-7 个工作日，邮寄 4-6 周 | 没有 SSN/ITIN 的非居民 |
| 通过代理代办 | $50-150 | 1-3 周 | 不想自己跑流程 |

**中国开发者的现实情况：** 你大概率没有 SSN（社会安全号），也没有 ITIN（个人纳税识别号）。这意味着不能用 IRS 官网在线申请（那个系统要求输入 SSN/ITIN）。

可行路径：
1. **传真 SS-4 表格给 IRS** — 填好 Form SS-4，传真到 IRS 国际部门（+1-855-215-1627 适用于非居民）。大约 4-7 个工作日收到回复。这是免费的。
2. **用代理代办** — Northwest、Firstbase 等都提供 EIN 代办服务，$50-150 不等。省事，但多花钱。
3. **Stripe Atlas 自动处理** — 如果你走 Stripe Atlas 路径，EIN 申请包含在 $500 服务里，他们帮你搞定。

EIN 拿到后，IRS 会给你一封确认信（CP 575 Notice）。这封信很重要，银行开户要用。

## 第六步：开银行账户

有了 LLC 的 Certificate of Organization + EIN + Operating Agreement，就可以开美国银行账户了。

**中国人远程可开的美国银行：**

| 银行 | 类型 | 月费 | 说明 |
|------|------|------|------|
| Mercury | 纯线上商业银行 | $0 | 最受独立开发者欢迎，申请流程全线上，支持 Stripe/Wise 入金 |
| Relay | 纯线上商业银行 | $0 | 和 Mercury 类似，审核略宽松 |
| Wise Business | 跨境账户 | $0（按交易收费） | 不是严格意义上的美国银行，但能拿到美国 ACH routing number |

**Mercury 开户流程：**
1. 官网注册：https://mercury.com
2. 填写公司信息（LLC 名称、EIN、注册州、业务描述）
3. 上传文件：Certificate of Organization、EIN 确认信、Operating Agreement、个人护照
4. 等待审核：通常 1-3 个工作日
5. 审核通过后，获得 checking account + routing number

Mercury 对独立开发者很友好，AI 产品、SaaS、数字产品这类业务描述基本都能通过。但如果你的业务描述写得太模糊（比如 "general consulting"），可能会被要求补充说明。

## 第七步：注册 Stripe

银行账户开好后，就可以注册 Stripe 了。

Stripe 注册需要：
- LLC 的公司信息（名称、EIN、注册地址）
- 银行账户信息（用于接收 Stripe 打款）
- 个人身份信息（护照、居住地址）
- 业务描述和网站 URL

**注意事项：**
- 注册地址填你的 Registered Agent 地址即可
- 业务描述要具体——不要写 "software"，写 "AI-powered writing assistant for English learners, subscription-based"
- 网站 URL 必须能打开，Landing Page 至少要有产品介绍和定价页面
- Stripe 审核通常 1-2 天，偶尔会要求补充材料

## 费用总结

走最经济路径（自己注册 Wyoming LLC + 传真申请 EIN + Mercury）：

| 项目 | 费用 |
|------|------|
| Wyoming LLC 注册费 | $100 |
| 注册代理（首年） | $100-125 |
| EIN 申请 | $0（自己传真） |
| Mercury 开户 | $0 |
| Stripe 注册 | $0 |
| **首年总计** | **$200-225** |
| **后续每年** | **$160-185**（州年报 $60 + 注册代理 $100-125） |

走省心路径（Stripe Atlas）：

| 项目 | 费用 |
|------|------|
| Stripe Atlas 全包 | $500 |
| **首年总计** | **$500** |
| **后续每年** | **$160-185**（州年报 + 注册代理续费） |

## 时间线总结

| 步骤 | 耗时 |
|------|------|
| 选州 + 选注册代理 | 1 天（做决定） |
| 提交 Articles of Organization | 1-3 个工作日 |
| 准备 Operating Agreement | 1 天 |
| 申请 EIN（传真方式） | 4-7 个工作日 |
| 开 Mercury 银行账户 | 1-3 个工作日 |
| 注册 Stripe | 1-2 个工作日 |
| **总计** | **2-4 周** |

如果走 Stripe Atlas，总时间差不多（他们也要帮你排队申请 EIN），但你不需要自己盯每一步。

## 常见坑

**1. LLC 名称被占用。** 提交前一定先在州务卿网站搜一下。Wyoming 的查询地址：https://wyobiz.wyo.gov/Business/FilingSearch.aspx

**2. EIN 申请被拒。** 最常见原因是 SS-4 表格填错了——Responsible Party 那栏应该填你自己的名字（不是 LLC 的名字），ID Number 那栏如果没有 SSN/ITIN 就填 "Foreign"。

**3. Mercury 开户被拒。** 业务描述太模糊、网站还没上线、或者同一个人名下已经有多个公司账户。被拒后可以补充材料重新申请，或者换 Relay 试试。

**4. 地址一致性。** LLC 注册地址、EIN 信上的地址、银行开户地址、Stripe 注册地址——这些最好保持一致（都用 Registered Agent 地址）。不一致容易触发审核。

**5. 忘记年报。** Wyoming 每年需要提交 Annual Report（网上填一下就行），截止日是 LLC 注册月份的第一天。忘了交就会被罚款，持续不交会被吊销。设个日历提醒。

---

*下一篇：[美国、香港、新加坡：三地公司怎么选](us-hk-sg-company-comparison.md)*
