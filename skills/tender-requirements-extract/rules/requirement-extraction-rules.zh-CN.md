# 要求提取

## L0
在保持可核验义务整体、逻辑及适用范围的前提下采用最细粒度。OR 组仍是一项具有备选条件的义务，不将备选项拆成分别必需的检查。

## L1
- 阅读全部授权相关条款、表格、脚注及被引用附件，记录实际文件状态。纯结构标题不是义务；标题真实的范围/条件随依赖正文一起提取，不编造重复父义务。
- 只拆分真正独立且主体、条件、后果仍完整的义务。同一义务的 AND 条件保留整体；OR 备选即使证明类型不同也保留整体。混合逻辑在准确引文和人类解释中保留括号及条件；顶层 `logic: and/or/single` 只作真实概括，确切嵌套表达式写入 `condition`/`notes`，不造未支持的嵌套 JSON。
- 每行需要 `requirement_id`、`source_file_id`、`location`、逐字 `source_quote`、`requirement_type` 和 `status`。保留标点、否定、量词、例外及相关上下文；不设会截掉例外的任意引文长度上限，保留必要原文并在 notes 单独解释。
- 可选字段是 `subject`、`condition`、`logic`、`quantifier`、`exception`、`proof_requirement`、`superseded_by`、`is_mandatory`、`notes`。涉及数值时，在这些支持的字符串中记录实际值、比较符、单位、分母、上限和舍入口径。未知操作数或分母明确列为局限，不视为零或通过；阈值按源文定义计算，不除以假定满分。
- 签字盖章在 `proof_requirement` 和 notes 保留指定主体、签署方式、印章类型、格式及 AND/OR 关系。“签章”等未定义措辞在适用原文未解释时保留歧义；图像在场不等于鉴真。
- 补遗遵循[补遗规则](amendment-handling-rules.zh-CN.md)。条款适用状态（`active`、`superseded`、`withdrawn`、`pending_review`）不等于投标响应状态；完全/部分/矛盾/未决响应写入发现说明或覆盖 notes，不将这些值写进要求 status。

## L2：覆盖与交付
coverage 项记录实际检查动作，仅用 `checked`、`failed`、`unchecked`；不在覆盖项添加 requirement_id 字段，发现通过 requirement_refs 与 bid_evidence 关联。`present`/`absence` 是投标证据类型，不是覆盖状态；缺失须列明覆盖相关同文件搜索范围的已查项，未知不等于缺失。

按项准确计数。每个清单文件都应被覆盖，或基于授权范围逐个用 `file_id: 非空理由` 排除，不能因不便或未读而排除。有理由的 failed/unchecked 可使账本核算闭合；审查未完成时报告仍须 partial_only/cannot_conclude。文件 pending/partial/failed 不能支持 checked 证据；只有真实建立新清单时才能拆分输入范围/版本，不为通过校验把失败文件改标成功。

采用实际来源 ID 和值，不复用示例模板 ID/计数。只产出自身负责贡献；总审协调跨角色覆盖并写唯一最终报告，独立 Evidence 验证六产物包并重读证据。

参见[分类](requirement-classification-rules.zh-CN.md)和[定位](location-format-rules.zh-CN.md)。
