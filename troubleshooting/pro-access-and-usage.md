# Pro 已开通，但模型入口或可用额度不符合预期怎么办？

> 最近核对：2026 年 9 月 12 日

遇到这种情况，我会先暂停新的购买，把订阅、登录、模型入口和用量分开检查。付款成功只能证明这一步的结果，不能单独证明目标账号、档位、模型开放和额度都符合预期。

## 先按看到的现象选路线

| 现象 | 先检查什么 | 暂时不要做什么 |
|---|---|---|
| 有付款记录，但目标套餐没出现 | 原订单结果、购买目标与当前登录账号 | 再买一笔相同商品 |
| 20× 显示续订安排完成，到期时间却没变 | 本次是否为到期自动扣费安排、扣费是否已完成 | 当成立即覆盖失败再下一单 |
| 20× 扣款失败、不可用或已变 Free | 原渠道账单、通知邮件与订阅是否终止 | 假定曾开通过就一定能重新购买 |
| 已显示 Pro，但 Codex 用量或功能像另一个账号 | 登录方式、账号和工作区 | 公开上传登录文件或凭据 |
| 订阅正常，但找不到 Astra 等模型 | 客户端、模型选择器与实际开放范围 | 仅凭模型名称再买一次订阅 |
| Pro 有效，但提示限额或用量不足 | 限额对应的窗口、重置时间与功能 | 假定续费或覆盖能保证全部重置 |
| 有额度，但回答不符合预期 | 任务材料、范围、设置与验收要求 | 把结果质量问题直接当成套餐错误 |

## 第一步：确认订阅本身

打开当前账号的订阅管理页，对照自己的购买记录，确认账号、目标档位、有效期或下次扣款时间。注意不同页面可能只显示“Pro”，不一定直接写出 5× / 20×；信息不足时继续核对，不要仅凭一个标签判断档位。

如果付款或订单还没有明确结果，回到原购买渠道查询。超过其说明时间仍无变化时，通过对应支持入口处理，不重复下单。已有订阅换档的人，也要复查 [付款前确认的账期与覆盖条件](../articles/pro-upgrade-renewal-checklist.md)。

**20× 老用户另看续订阶段：** PlusGO 的“续订安排已完成”并不立即延长到期日，需等本次到期扣费成功后确认新周期。若订阅已经终止，暂停期间无法重新新购；仍显示 20× 但扣费失败时，是否存在可恢复的账单要由原渠道核实。见 [20× 续订与账单排查](../articles/pro-20x-pause-and-renewal.md#renewal-status)。

## 第二步：确认正在使用哪一种登录方式

我会在客户端的账号菜单中确认当前账号和工作区，再与购买目标比较。若使用 Codex，尤其要区分：

- **ChatGPT 账号登录**：使用订阅对应的访问路径，仍受账号和工作区条件约束。
- **API 凭据登录**：属于单独的按量计费路径，不使用个人 Pro 的包含用量。

两种方式的可用功能也可能不同。给 ChatGPT 账号购买 Pro，不会让另一套 API 账单自动变成订阅账单。[登录方式与计费边界](https://learn.chatgpt.com/docs/auth)

确认登录错误时，在自己的设备上使用正常退出、登录流程。不要上传认证文件、完整 Session、Cookie 或访问凭据来求助，也不要把凭据交给陌生人代查。

## 第三步：检查模型入口，而不是只看发布消息

在实际使用的客户端查看模型与推理设置。ChatGPT 桌面端和 Work 的模型控件位于输入框附近；Codex CLI 可用 `/model` 查看可选项。先确认客户端版本与设置，再核对自己账号实际出现的选项。[模型选择与可用性](https://learn.chatgpt.com/docs/models)

需要注意：

- Work / Codex 的模型说明，不能直接当作普通 Chat 的权益列表。
- 可用性受开放进度、登录方式和客户端影响；不同界面不一定同时出现同一个选项。
- 在公司管理的工作区中使用时，先确认当前工作区和相应权限，必要时联系管理员。
- 更新客户端可以排除部分界面或兼容问题，但不会自动授予账号没有的访问权限。
- Astra 需要 Codex CLI `0.153.0` 或更新版本；桌面端手动检查 `Menu → Check for Updates`，即使刚点过自动更新也再确认一次。
- 不要通过手填隐藏名称或照抄他人的配置，把“可以填写模型名”理解为“已获得使用权”。

普通 Chat 中的 Astra 名称是 GPT-6 Pro，当前包含在 Pro 5×、20×、Business 与 Enterprise；Plus 包含 Work / Codex 中的 Astra，不包含普通 Chat 的 GPT-6 Pro。[官方入口与版本要求](https://help.openai.com/en/articles/20001354-gpt-56-in-chatgpt/)。展开比较见 [Astra 选档指南](https://github.com/duck-gogo/chatgpt-plus-tutorial/blob/main/articles/gpt-6-astra-which-plan.md)。订阅和登录正常但缺入口时，先处理入口问题，不重复购买。

## 第四步：查看具体限额与重置时间

打开 [Usage](https://chatgpt.com/codex/settings/usage)，记录页面显示的限额名称、已用或剩余口径、重置时间。Codex CLI 也可用 `/status` 查看。不要把会员到期日和用量重置时间当成同一个时间点。[用量查询](https://learn.chatgpt.com/docs/pricing#where-can-i-see-my-current-usage-limits)

Work 与 Codex 共享用量；并行任务、上下文、模型和推理设置都会影响消耗。还要核对提示是否来自某个单独功能，而不是套餐的通用窗口。20× 不能理解成所有任务与功能不限量。[用量边界](https://learn.chatgpt.com/docs/pricing#what-are-the-usage-limits-for-my-plan)

如果提示来自普通 Chat 的 GPT-6 Pro，按 [主指南的 Chat 限额表](../README.md#astra) 排查：5× 档的 GPT-6 Pro 与 Sol Pro 共用每周额度，切换不能绕过共享上限。20× 用完 GPT-6 Pro 周额度后会回退到 GPT-5.6 Thinking 的 Medium；如 Sol Pro 仍有余量，可在模型菜单选择 GPT-5.6 Sol，再选 Pro，仍受其日额度及两模型合计日额度约束。[官方限额与回退说明](https://help.openai.com/en/articles/20001354-gpt-56-in-chatgpt/)。模型受限不等于会员掉订阅，Codex 点数也不保证解除这个限制。

如果刚覆盖或换档，不要据此假定额度必然全满；回看本次购买条件与账号显示。页面数据似乎有误、重置后仍不符合预期时，保留时间与脱敏提示，联系对应支持方核对。

频繁用完但没有异常提示，可以用 [一周用量记录](../articles/pro-usage-journal.md) 判断持续需求。只偶尔缺少用量时，再比较 [等待重置、点数与 Reset](https://github.com/duck-gogo/chatgpt-plus-tutorial/blob/main/articles/codex-credits-recharge-guide.md)，不要把它们当成同一种权益。

## 求助时准备哪些材料

向确认过的支持渠道说明：发生时间与时区、客户端及版本、实际提示、当前套餐、是否刚换档，以及已做过哪些检查。订单问题仅在原购买渠道的私密沟通中提供必要的订单信息。

公开提问只保留问题描述和脱敏内容，去掉邮箱、手机号、订单号、支付信息、公司文件和会话凭据。文档中的失效链接或错误表述可以走 [纠错入口](../CONTRIBUTING.md)；那里不是账号或订单售后入口。

如果订阅、模型和用量都正常，只有结果质量不满意，可以继续看 [回答质量异常排查](https://github.com/duck-gogo/chatgpt-plus-tutorial/blob/main/troubleshooting/chatgpt-answer-quality.md)。

[返回开通验收](../README.md#steps) · [专题目录](../articles/README.md) · [资料索引](../SOURCES.md)
