# 00 ChatGPT Read First

## 一、项目用途

本仓库是一个可长期复用的 TikTok Shop US 商品卡规划系统，用于围绕我方真实产品资料、竞品商品卡、竞品图片与长期知识卡，生成适合美国市场的完整商品卡方案。

核心支持内容包括：

- 最大卖点提取
- 同一产品多个卖家竞品聚合
- 标题
- 搜索关键词
- 主图 6–8 张
- 详情图
- 商品描述
- 5 点商品亮点
- 每张图单独的 ChatGPT 生图提示词

本文件只作为 ChatGPT 通过 GitHub 应用读取仓库时的统一入口、索引和执行协议，不复制全部项目正文；具体规则必须继续读取对应模块文件。

## 二、唯一知识源

- `main` 分支是正式生产版本。
- 其他任务分支、实验分支、临时修复分支都不是正式版本。
- ChatGPT 每次开始任务时，应读取 `main` 分支最新内容作为唯一正式知识源。
- `changelog.md` 用于判断最近更新、规则变化和新增能力；读取入口文件后必须优先查看。


## 三、日常运行优先读取

日常完整商品卡任务优先读取：

1. `CHATGPT_RUNTIME_BUNDLE.md`：运行时精简规则包，用于快速执行常规完整商品卡规划。
2. `changelog.md`：确认最近规则变化、运行包版本和来源提交。
3. 与当前产品相关的产品组、产品档案或竞品分析。
4. 必要时读取专项策略文件。

`CHATGPT_RUNTIME_BUNDLE.md` 是日常执行精简包；专项文件仍是完整规则源。ChatGPT 不需要日常无差别读取全部仓库，不得使用旧对话规则替代 `main` 最新运行包。

## 四、专项任务读取规则

### 完整商品卡规划

读取：

- `CHATGPT_RUNTIME_BUNDLE.md`
- 当前产品资料
- 当前产品参考图
- 对应竞品产品组

### 仅做标题和关键词

读取：

- `CHATGPT_RUNTIME_BUNDLE.md`
- 必要时读取 `06_title_strategy.md`
- 必要时读取 `07_search_keyword_strategy.md`

### 仅做图片规划

读取：

- `CHATGPT_RUNTIME_BUNDLE.md`
- `08_main_image_strategy.md`
- `09_detail_image_strategy.md`
- `18_competitor_image_analysis.md`

### 仅做 ChatGPT 生图提示词

读取：

- `CHATGPT_RUNTIME_BUNDLE.md`
- `19_chatgpt_image_prompt_module.md`
- `20_image_prompt_output_template.md`
- 当前产品参考图

### 竞品产品组聚合

读取：

- `CHATGPT_RUNTIME_BUNDLE.md`
- `04_competitor_listing_absorption.md`
- `18_competitor_image_analysis.md`
- 对应竞品资料和分析报告

## 五、完整源文件读取顺序

ChatGPT 不上传整个仓库到 Project 时，应按以下顺序读取核心文件：

1. `00_CHATGPT_READ_FIRST.md`：统一入口、读取顺序、任务选择规则和执行协议。
2. `CHATGPT_RUNTIME_BUNDLE.md`：日常运行优先读取的精简规则包。
3. `changelog.md`：最近更新、规则变化、已补齐能力和历史修复记录。
4. `00_system_control.md`：系统总控、工作顺序、基础边界、竞品资料读取控制和多卖家聚合控制。
5. `01_input_requirements.md`：用户输入、我方产品资料、竞品资料和图片资料的最低要求。
6. `02_output_template.md`：最终商品卡输出结构和模块顺序。
7. `03_core_selling_point_extraction.md`：候选卖点提取、评分和最大卖点确定方法。
8. `04_competitor_listing_absorption.md`：竞品商品卡拆解、吸收、转化和同产品多卖家聚合方法。
9. `06_title_strategy.md`：TikTok Shop US 标题规划规则。
10. `07_search_keyword_strategy.md`：搜索关键词与流量词规划规则。
11. `08_main_image_strategy.md`：主图 6–8 张的顺序、功能和转化逻辑。
12. `09_detail_image_strategy.md`：详情图内容结构、信息层级和展示顺序。
13. `10_product_description_strategy.md`：商品描述写法和信息组织。
14. `11_highlights_strategy.md`：5 点商品亮点写法。
15. `12_us_native_ecommerce_language.md`：美国本土电商英文表达规则。
16. `15_quality_review_checklist.md`：最终质量检查清单。
17. `18_competitor_image_analysis.md`：竞品主图、详情图、SKU 图与产品参考图的图片分析方法。
18. `19_chatgpt_image_prompt_module.md`：ChatGPT 生图提示词生成规则。
19. `20_image_prompt_output_template.md`：单图提示词输出格式。
20. `raw_inputs/竞品资料/产品分组说明.txt`：当前竞品产品组关系。
21. `raw_inputs/研究记录/竞品资料读取报告.md`：当前竞品资料读取与图片分析记录。
22. `knowledge_cards/`：通用知识卡；只在对应任务需要时选择性读取。
23. `examples/`：输入、输出、图片分析和提示词示例；只在需要对齐格式时读取。

## 六、按任务选择性读取（源文件回退）

### 商品标题任务

必须读取：

- `00_CHATGPT_READ_FIRST.md`
- `changelog.md`
- `00_system_control.md`
- `01_input_requirements.md`
- `03_core_selling_point_extraction.md`
- `04_competitor_listing_absorption.md`
- `06_title_strategy.md`
- `07_search_keyword_strategy.md`
- `12_us_native_ecommerce_language.md`
- `13_tiktokshop_listing_traffic_logic.md`
- `knowledge_cards/tiktokshop_seo_cards.md`
- `knowledge_cards/us_ecommerce_copy_cards.md`
- 相关产品组资料与用户当前提供的我方产品资料

### 图片规划任务

必须读取：

- `00_CHATGPT_READ_FIRST.md`
- `changelog.md`
- `00_system_control.md`
- `03_core_selling_point_extraction.md`
- `04_competitor_listing_absorption.md`
- `08_main_image_strategy.md`
- `09_detail_image_strategy.md`
- `18_competitor_image_analysis.md`
- `knowledge_cards/product_image_conversion_cards.md`
- `knowledge_cards/product_image_layout_cards.md`
- 相关竞品主图、详情图、SKU 图和用户当前上传的产品参考图

### ChatGPT 生图提示词任务

必须读取：

- `00_CHATGPT_READ_FIRST.md`
- `changelog.md`
- `00_system_control.md`
- `08_main_image_strategy.md`
- `09_detail_image_strategy.md`
- `18_competitor_image_analysis.md`
- `19_chatgpt_image_prompt_module.md`
- `20_image_prompt_output_template.md`
- `knowledge_cards/chatgpt_image_prompt_cards.md`
- 每张图对应的图片规划、画面目标、文字内容和用户当前产品参考图

### 竞品聚合任务

必须读取：

- `00_CHATGPT_READ_FIRST.md`
- `changelog.md`
- `00_system_control.md`
- `04_competitor_listing_absorption.md`
- `18_competitor_image_analysis.md`
- `raw_inputs/竞品资料/产品分组说明.txt`
- `raw_inputs/研究记录/竞品资料读取报告.md`
- 对应产品组下每个竞品卖家的标题、SKU、链接、主图、详情图和产品参考图

### 完整商品卡任务

必须读取：

- `00_CHATGPT_READ_FIRST.md`
- `changelog.md`
- `00_system_control.md`
- `01_input_requirements.md`
- `02_output_template.md`
- `03_core_selling_point_extraction.md`
- `04_competitor_listing_absorption.md`
- `06_title_strategy.md`
- `07_search_keyword_strategy.md`
- `08_main_image_strategy.md`
- `09_detail_image_strategy.md`
- `10_product_description_strategy.md`
- `11_highlights_strategy.md`
- `12_us_native_ecommerce_language.md`
- `13_tiktokshop_listing_traffic_logic.md`
- `14_shopping_psychology.md`
- `15_quality_review_checklist.md`
- `16_content_boundary_and_claim_handling.md`
- `18_competitor_image_analysis.md`
- `19_chatgpt_image_prompt_module.md`
- `20_image_prompt_output_template.md`
- 相关 `knowledge_cards/`
- 相关产品组资料、竞品图片资料、用户当前我方产品资料和用户当前上传的产品参考图

## 七、产品组索引

当前竞品产品组索引如下：

- 电动水枪
  - 电动水枪竞品1
  - 电动水枪竞品2
  - 关系：同一款产品的两个不同卖家商品卡

- 恐龙沙盒
  - 恐龙沙盒竞品1

- 飞碟泡泡机
  - 飞碟泡泡机竞品1

产品组关系以 `raw_inputs/竞品资料/产品分组说明.txt` 为准；如该文件后续更新，应优先使用该文件而不是本索引的旧内容。

## 八、运行流程

固定执行顺序：

1. 读取用户当前产品资料
2. 读取相关产品组
3. 聚合多个竞品样本
4. 提取候选卖点
5. 确定最大卖点
6. 规划文字商品卡
7. 规划图片顺序
8. 输出每张图的 ChatGPT 生图提示词
9. 质量检查

## 九、信息优先级

1. 用户当前提供的我方真实产品信息
2. 用户当前上传的产品参考图
3. 仓库产品档案
4. 仓库竞品产品组分析
5. 仓库通用知识卡
6. 历史聊天信息

## 十、禁止行为

- 不得简单拼接多个竞品的全部卖点
- 不得把不同规格混成一个 SKU
- 不得忽略用户当前上传的产品资料
- 不得把所有图片提示词合并成一条
- 不得只根据竞品文件夹名称推测图片内容
- 不得使用旧任务分支内容覆盖 `main` 版本
