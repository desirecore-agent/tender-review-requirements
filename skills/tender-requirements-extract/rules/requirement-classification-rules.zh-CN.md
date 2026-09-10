# 要求分类

## L0
义务主题、违反后果和发现的确定性分别判断；只使用共享 `requirement_type` 枚举。证书未见、二元检查或类别未知不证明应否决，也不要求默认高严重度。

## L1
| 值 | 有来源依据的用途 |
|---|---|
| `qualification` | 参与前提、资质或履约能力 |
| `substantive_response` | 必需方案内容、履约或承诺 |
| `scoring` | 评分公式、分配、阈值或评审标准 |
| `submission` | 递交、时间、格式、份数及签字盖章程序 |
| `compliance` | 已确认适用的明确合规/法律义务 |
| `other` | 已识别义务不属于已知主题；解释不确定性 |

判定前阅读条款及其引用规定。同段若分别规定独立的参与和评分义务，保留两项并交叉引用；若是一个复合义务，保留整体逻辑，选择最有依据的主题，在 notes 说明其他方面。不用严重度层级决定类型。评分条款可能另含明确最低通过阈值，不假设所有失分均无影响，也不假设所有评分均意味着否决。

`is_mandatory` 在契约中含义严格：适用原文规定不满足将否决时为 true，已明确仅评分扣减时为 false；后果未确定时省略并在 notes 解释。一般“必须”本身不证明否决。准确后果引文及位置写入 notes，或在后果另载他处时建立独立有来源条款行。不把 `disqualification` 或 `eligibility` 当作新枚举输出。

## L2
发现 `severity` 表示影响（`potential_rejection`、`high`、`medium`、`low`、`informational`），`certainty` 表示证据把握（`confirmed`、`likely`、`uncertain`、`unverified`）；分别说明有依据的影响和证据局限。潜在否决必须有明确适用的否决依据、准确要求引用和投标侧证据；确实缺失须有同文件已完成搜索覆盖，未读或不可辨认内容不能证明确定缺失。

作者设置 `open` 或 `pending_review`；仅独立 Evidence 产出 `reviewed_confirmed`、`reviewed_downgraded`、`reviewed_withdrawn`，并保留可追溯理由。正式资格及否决决定由有权人员作出；优先处理可信严重风险，不用升级严重度弥补不确定性。

参见[补遗](amendment-handling-rules.zh-CN.md)及[提取](requirement-extraction-rules.zh-CN.md)。
