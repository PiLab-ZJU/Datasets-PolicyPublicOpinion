# 政策舆情项目数据集汇总

## 政策舆情研究数据集

### 三孩相关政策舆情数据
本数据源自2023年国家级大学生创新创业项目《三孩”政策下的网络舆情演化和网民用户画像：基于新浪微博数据的研究》，项目参与人：韦奖沂，喻锐，吕超。
#### 数据背景

本研究围绕“三孩”相关政策及其引发的舆论讨论展开，旨在通过分析新浪微博用户对“三孩”政策的博文、评论、转发等数据，探讨政策相关的公众情感和舆论态势。

- **数据来源**：通过爬取新浪微博中与“三孩”相关的词条及其讨论内容。
- **关键词样例**：如“#三孩生育政策来了#”、“#三孩政策会带来哪些改变#”、“#三孩放开后父母压力有多大#”。
- **数据收集方法**：通过话题链接的方式，精确获取与政策相关性更强的讨论内容，并对数据进行清洗降噪。

#### 数据集的数量

1. **博文数据**
   - 总量：19,068条。
   - 清洗后有效数据：19,068条。

2. **评论数据**
   - 对评论数达到100的博文进行爬取。
   - 清洗后有效数据：27,103条。

3. **转发数据**
   - 对转发量大于10的博文进行爬取。
   - 清洗后有效数据：8,551条。

4. **合并数据**
   - 在主题分析中合并博文、评论、转发数据，共计54,722条。

5. **用户信息数据**
   - 针对发布博文和评论的用户，收集性别、IP、认证等信息。
   - 总量：45,715条有效用户数据。

#### 数据集包含的具体维度与字段

1. **博文数据字段**
   - `content`：微博文本内容。
   - `user_id`：发布者ID。
   - `timestamp`：发布时间。
   - `likes_count`：点赞数。
   - `comments_count`：评论数。
   - `reposts_count`：转发数。

2. **评论数据字段**
   - `comment_content`：评论内容。
   - `comment_user_id`：评论者ID。
   - `comment_likes_count`：评论点赞数。

3. **转发数据字段**
   - `repost_content`：转发内容。
   - `repost_user_id`：转发者ID。
   - `repost_timestamp`：转发时间。

4. **用户信息字段**
   - `gender`：性别。
   - `ip_location`：IP地址。
   - `user_verification`：认证信息。

#### 数据预处理

1. **清洗操作**
   - 删除无文本内容的博文、评论和转发。
   - 去除重复和无效内容，如“转发微博”、“快转微博”。

2. **合并处理**
   - 将博文、评论和转发数据合并形成用于主题分析的整体数据集。

#### 潜在研究话题总结

1. **政策舆论情感分析**
   - 分析“三孩”政策相关博文、评论和转发中的情感倾向（积极、中性、消极）。

2. **舆论传播路径与模式**
   - 研究博文、评论与转发之间的传播路径与网络互动模式。

3. **用户特征与观点分布**
   - 探讨性别、地域、认证信息等用户特征对政策讨论观点分布的影响。

4. **主题挖掘与演化**
   - 通过LDA主题分析挖掘讨论热点，研究舆论主题的变化趋势。

5. **政策传播与公众反应**
   - 结合传播量与情感分析，探讨公众对“三孩”政策的接受度与反应模式。

6. **高互动内容特征**
   - 分析评论数或转发数高的博文特征，探索哪些内容更易引发互动。

该数据集为理解“三孩”政策引发的舆论态势、情感分布及传播规律提供了重要的分析基础，同时有助于研究公众对社会政策的接受与反应模式。



### 房地产税试点政策舆情数据
本数据源自2018级信息资源管理专业本科毕业论文《政策舆情情感图谱研究--以“房地产税”试点政策相关微博为例》，毕业生邵佳攀。
#### 数据背景

本研究的数据集来源于新浪微博，围绕“房地产税”相关舆情展开分析。以新浪微博的微指数作为衡量指标，研究从舆情潜伏期、爆发期到平息期的舆情发展趋势。研究时间范围为2021年10月9日至2021年11月7日。

- **舆情阶段划分**：
  - 潜伏期：2021年10月9日至10月16日。
  - 爆发期：2021年10月17日至10月30日。
  - 平息期：2021年10月31日至11月7日。

#### 数据集的数量

1. **原创微博数据**
   - 爬取总量：6,911条。
   - 清洗后有效数据：6,825条。

2. **人工情感标注数据**
   - 总量：选取原创微博数据的一半（3,413条）。
   - 数据随机排序后，确保时间分布均匀。

#### 数据集包含的具体维度与字段

1. **原创微博字段**
   - `time`：发布时间。
   - `content`：微博文本内容。
   - `likes_count`：点赞数。
   - `comments_count`：评论数。
   - `reposts_count`：转发数。

2. **情感标注字段**
   - `sentiment`：情感倾向，分为积极、中性和消极三类。

3. **情感标注原则**
   - 情感基于微博整体倾向，而非单纯针对“房地产税”政策本身。
   - 介绍性或不明确情感的文本标注为中性。

#### 数据预处理

1. **清洗流程**
   - 删除带有“房地产税”标签但实际内容无关的微博。
   - 确保数据与微指数时间分布一致。

2. **人工标注信度**
   - 通过随机抽样的300条数据进行检验，准确性为90.67%。

#### 潜在研究话题总结

1. **舆情发展阶段分析**
   - 探讨“房地产税”相关舆情在潜伏期、爆发期和平息期的情感倾向与变化。

2. **情感分类模型评估**
   - 比较SVM、BERT及基于情感词典的算法在情感分类上的准确性。

3. **舆情热点分析**
   - 基于时间分布和微指数，识别舆情高峰期的核心热点话题。

4. **情感驱动因素研究**
   - 分析不同情感倾向的微博内容特征，探讨导致积极、消极、中性情感的主要因素。

5. **政策传播与公众反应**
   - 研究政策相关舆情的传播路径及公众对政策的反应模式。

6. **标注方法优化**
   - 探讨人工情感标注的优化策略，提高标注信度与效率。

通过上述分析，该数据集为理解政策舆情动态、情感分类技术评估及传播机制提供了数据支持和研究方向。



### 上海非沪籍高校毕业生落户相关政策的舆情数据
本数据源自2019级信息资源管理专业本科毕业论文《上海非沪籍高校毕业生落户政策网络舆情演化研究》，毕业生林晨。
#### 数据背景

本研究的数据集来源于新浪微博，主要围绕上海非沪籍高校毕业生落户政策相关的网络舆情演化分析。
- **数据来源**：通过 Python 网络爬虫从新浪微博平台获取。
- **关键词**："上海 毕业 落户"和"上海 应届 落户"。
- **时间范围**：2018年1月1日至2022年12月31日。
- **数据类型**：包括博文数据和评论数据。

#### 数据集的数量

1. **博文数据**
   - 原始数据数量：
     - "上海 毕业 落户"关键词：14,540条。
     - "上海 应届 落户"关键词：8,028条。
   - 合并后博文数据：18,274条。
   - 清洗后博文数据：9,032条。

2. **评论数据**
   - 原始数据：19,766条（覆盖2018年、2020年、2021年、2022年）。
   - 清洗后评论数据：16,699条。

3. **合并数据**
   - 合并博文数据与评论数据，最终数据总量为25,731条。

#### 数据集包含的具体维度与字段

1. **博文数据字段**
   - `keywords`：检索关键词。
   - `time`：发布时间。
   - `user_id`：发布者ID。
   - `screen_name`：发布者昵称。
   - `content`：博文内容。
   - `mid`：博文ID。
   - `url`：博文链接。
   - `reposts_count`：转发数。
   - `comments_count`：评论数。
   - `attitudes_count`：点赞数。

2. **评论数据字段**
   - `time`：评论发布时间。
   - `user_id`：发布者ID。
   - `screen_name`：发布者昵称。
   - `floor`：评论楼层。
   - `content`：评论内容。
   - `attitudes_count`：点赞数。

3. **合并字段**
   - `type`：数据类型（`main_body` 表示博文，`comment` 表示评论）。
   - `seg`：分词结果。
   - `stop`：去停用词结果。

#### 数据清洗与预处理

1. **博文数据清洗**
   - 合并两组关键词爬取的数据。
   - 去除重复博文（以`mid`和`url`为标准）。
   - 删除重复内容和与主题无关的博文（通过关键字筛选）。

2. **评论数据清洗**
   - 合并四年的评论数据。
   - 删除空值、纯数字或符号的评论。
   - 去重操作。

3. **最终数据**
   - 博文和评论数据按字段合并，得到25,731条清洗后的数据。

#### 潜在研究话题总结

1. **舆情演化分析**
   - 分析上海非沪籍高校毕业生落户政策在微博上的舆情变化趋势，识别讨论热点和高峰时段。

2. **政策影响力评估**
   - 通过博文和评论的情感分析，评估政策实施前后公众的态度变化。

3. **信息传播路径研究**
   - 研究博文的转发、评论与点赞行为的传播规律，挖掘舆情扩散机制。

4. **用户行为分析**
   - 分析不同用户群体（如普通用户、媒体、大V）的参与行为及其对舆情的影响。

5. **文本挖掘与话题提取**
   - 基于分词结果与高频词分析，挖掘公众讨论的核心主题。

6. **跨年份比较**
   - 对比2018年至2022年间舆情变化，探索政策调整与舆论响应之间的关联。

该数据集为网络舆情分析、政策评估及传播研究提供了丰富的研究基础。





### 《互联网信息服务算法推荐管理规定》政策舆情数据
本数据源自2020级信息资源管理专业本科毕业论文《我国算法治理政策网络舆情动态演化研究——以《互联网信息服务算法推荐管理规定》为例》，毕业生施若夷。

#### 数据集背景
- **研究主题**：围绕中国算法治理政策（《互联网信息服务算法推荐管理规定》，简称《算法规定》）在新浪微博平台上的舆情讨论。
- **时间范围**：数据覆盖从2021年8月27日（《算法规定》征求意见稿发布）到2022年8月26日的时间周期，旨在分析网民在政策不同阶段（征求意见、出台、实施等）的情感与观点变化。
- **研究平台**：新浪微博，一个在时事、政治、娱乐等领域具有重要影响力的社交网络媒体。

#### 数据来源与数量
- **总数据量**：共收集24,506条数据，分为博文数据和评论数据。
  - **博文数据**：爬取了15,568条相关博文。
  - **评论数据**：包括5,657条一级评论和3,281条二级评论，总计8,938条评论数据。
- **数据采集工具**：八爪鱼采集器，以“天”或“小时”为单位进行爬取。

#### 数据预处理
- **清洗操作**：
  - 删除重复值、缺失值和无意义广告信息。
  - 移除微博中的表情、符号、特殊字符等无效内容。
  - 经过清洗后保留有效数据：
    - **博文数据**：14,131条。
    - **评论数据**：6,068条。
- **分词与去停用词**：
  - 使用Python的`jieba`分词工具对文本进行分词。
  - 利用哈工大、百度、四川大学停用词表以及自定义停用词表清除冗余信息。
  - 去除了空格、标点符号、数字以及长度为1的词语。

#### 数据包含的具体维度与字段
- **博文数据**：
  - 博文文本、微博ID、发布用户ID、发布时间、发布地点、发布渠道、点赞数、评论数、转发数。
- **评论数据**：
  - 文本内容、评论时间、评论者ID、评论地点等。

#### 潜在研究话题
1. **政策舆情演变分析**：
   - 分析《算法规定》在各阶段（如征求意见、审议通过、实施等）网民情感和观点的变化趋势。
2. **公众对算法治理政策的情感倾向**：
   - 利用情感分析技术，探讨网民对政策的支持、质疑或反对的态度分布。
3. **舆论传播特点研究**：
   - 分析微博博文和评论的互动模式，探讨点赞、转发、评论数量对舆情传播的影响。
4. **平台数据特性分析**：
   - 比较一级评论和二级评论的数据特性，研究深层次讨论和初级表达的异同。
5. **算法推荐的社会影响**：
   - 探讨网民对《算法规定》中热点问题（如算法透明性、隐私保护等）的关注点和意见。
6. **政策话题中的语言特征**：
   - 通过分词和词频统计，挖掘舆情话题中的高频词汇和核心讨论主题。

该数据集为政策舆情研究提供了扎实的基础，能够支持情感分析、主题提取及传播机制研究等多种方向的深入探索。

### “调休”政策舆情数据
本数据源自2020级信息资源管理专业本科毕业论文《我国休假制度网络舆情的主题建模与情感分析》，毕业生赵奕超。

#### 数据集背景
- **研究背景**：数据集基于2023年微博话题“调休”相关的数据，旨在探讨公众对调休这一现象的情感和态度。
- **数据来源**：通过EasySpider爬取微博中的话题“调休”，以特定规则收集热度排名前500的话题评论。

#### 数据集数量
- **初始数据量**：共获得 **23,501 条**数据。
- **清洗后数据量**：经过人工筛选后，保留了 **11,785 条**适用于研究的微博评论数据。

#### 数据采集维度
- **时间规则**：
  - 非节假日：以周为单位爬取。
  - 节假日（如国庆、春节等）：以日为单位爬取。
- **采集内容**：热度排名前500的话题评论。

#### 数据处理
- **人工筛选**：去除以下情况的评论：
  1. 含有营销推广或官方通告。
  2. 内容与“调休”话题无关。
  3. 全由表情包或图片组成。
  4. 无法正确表意的评论。
- **文本清洗**：去除与情感分析、主题提取无关的标点符号和停用词。
- **情感标注**：
  - 针对“说反话”“阴阳”等难以辨别的评论进行人工情感标注。
  - 标注类型包括：积极、中性、消极。

#### 标注信度保证
- 由一人完成标注，另两人抽样校验并对争议结果重新标注。

#### 数据集潜在研究话题
1. **公众对调休现象的情感倾向**：
   - 分析公众对调休的消极、中性、积极态度分布。
2. **话题热度与情感之间的关联**：
   - 探讨评论热度（如点赞量）与情感类型之间的关系。
3. **社会热点与情感演化**：
   - 分析不同时间节点（如节假日前后）公众情感的变化趋势。
4. **语言表达中的讽刺与“阴阳”现象**：
   - 深入研究中文日常表达中的反语现象在舆论中的影响。
5. **微博平台的舆情传播特征**：
   - 研究平台特性如何影响公众的情感表达和讨论深度。

该数据集为分析调休相关舆情提供了详实的基础，特别适用于情感分析和主题提取领域的研究。



### 《新冠疫情紧急响应政策、新冠疫情公共卫生》政策舆情数据
该数据在疫情期间，从新浪微博收集了新冠疫情紧急响应政策、新冠疫情公共卫生政策的网络舆情数据。

数据集爬取了疫情背景下微博文本与评论，包括（blog_csv.csv和comments_csv.csv两个文件夹），共包含新冠疫情紧急响应政策、新冠疫情公共卫生政策的网络舆情数据：14175条微博数据和1292条微博评论数据。

包含字段如下：
blog_csv.csv
-  微博id
-  发布者昵称
-  发布者性别
-  发布者地区
-  发布者关注数
-  发布者粉丝数
-  微博正文
-  发布时间
-  点赞数
-  转发数
-  评论数

comments_csv.csv
-  评论者主页
-  评论者昵称
-  评论者性别
-  评论者所在地
-  评论者微博数
-  评论者关注数
-  评论者粉丝数
-  评论内容
-  评论获赞数
-  评论发布时间

本数据集提供了关于新冠疫情紧急响应政策和公共卫生政策的宝贵见解，特别是这些政策在公众舆论中的接受度、理解程度以及人们的行为反应。通过分析微博平台上的讨论和互动，研究人员能够深入了解公众对政府措施的态度和看法，识别出信息传播的有效性，以及发现可能存在的误解或谣言。

### 个人信息和隐私保护政策舆情数据
该数据以“隐私保护政策”、“个人信息保护法”等关键词，从新浪微博爬取个人信息和隐私保护政策数据。

数据集（./output.csv）共包含从2020年1月1日至2024年12月31日的1277条有关个人信息保护法和隐私保护政策的舆情数据。
字段释义如下：

- 微博id：微博的id，为一串数字形式
- 微博bid：微博的bid
- 微博内容：微博正文
- 头条文章url：微博中头条文章的url，若某微博中不存在头条文章，则该值为''
- 原始图片url：原创微博图片和转发微博转发理由中图片的url，若某条微博存在多张图片，则每个url以英文逗号分隔，若没有图片则值为''
- 视频url: 微博中的视频url和Live Photo中的视频url，若某条微博存在多个视频，则每个url以英文分号分隔，若没有视频则值为''
- 微博发布位置：位置微博中的发布位置
- 微博发布时间：微博发布时的时间，精确到天
- 点赞数：微博被赞的数量
- 转发数：微博被转发的数量
- 评论数：微博被评论的数量
- 微博发布工具：微博的发布工具，如iPhone客户端、HUAWEI Mate 20 Pro等，若没有则值为''
- 话题：微博话题，即两个#中的内容，若存在多个话题，每个url以英文逗号分隔，若没有则值为''
- @用户：微博@的用户，若存在多个@用户，每个url以英文逗号分隔，若没有则值为''
- 原始微博id：为转发微博所特有，是转发微博中那条被转发微博的id，那条被转发的微博也会存储，字段和原创微博一样，只是它的本字段为空
- 结果文件：保存在当前目录“结果文件”文件夹下以关键词为名的文件夹里
- 微博图片：微博中的图片，保存在以关键词为名的文件夹下的images文件夹里
- 微博视频：微博中的视频，保存在以关键词为名的文件夹下的videos文件夹里
- user_authentication：微博用户类型，值分别是蓝v，黄v，红v，金v和普通用户

该数据集它为研究个人信息保护法的公众认知度、社会反响以及隐私保护政策的实际应用提供了宝贵的实证资料。

## 社交媒体研究数据集

### 7·20河南暴雨求助微博数据集

### 数据集基本信息总结

#### 基本内容背景

本研究旨在探索社交媒体数据在自然灾害救助需求挖掘中的应用，提出基于大语言模型的分级多任务需求挖掘框架。研究以2021年河南“7.20”暴雨事件为案例，通过分析微博数据，挖掘细粒度的救助需求特征与规律，提出政策建议。

- **事件背景**：
  - 2021年7月，河南省遭遇特大暴雨，引发严重洪涝灾害。
  - 直接经济损失：1200.6亿元。
  - 微博上28个事件相关话题阅读量超过1亿。
- **研究目标**：
  - 提出基于大语言模型的救助需求挖掘框架。
  - 分析需求主体、内容、地点等要素的特征与规律。
  - 提出政策建议以优化救援行动。

#### 数据集的数量

1. **微博数据**
   - 时间范围：2021年7月10日至2021年8月31日。
   - 总量：1,139,221条微博文本。

2. **用户信息**
   - 数据总量：超过31万条用户信息。

#### 数据集包含的具体维度与字段

1. **微博数据字段**
   - `tweet_id`：微博ID。
   - `content`：微博文本内容。
   - `date`：发布时间。
   - `likes_count`：点赞数。
   - `reposts_count`：转发数。
   - `comments_count`：评论数。

2. **用户信息字段**
   - `user_id`：用户ID。
   - `username`：用户名。
   - `gender`：用户性别。
   - `location`：用户位置。
   - `followers_count`：粉丝数量。
   - `following_count`：关注数量。

3. **需求要素字段**（从文本中抽取）
   - `需求主体`：提出需求的用户或机构。
   - `需求内容`：需求的具体描述（如物资、救援、疏散等）。
   - `需求地点`：需求发生的地理位置。

#### 数据预处理与技术流程

1. **数据爬取**
   - 使用Python的Scrapy框架编写爬虫。
   - 收集微博文本与用户信息数据。

2. **数据清洗**
   - 去除无效或噪声数据。
   - 标注与抽取救助需求的主体、内容与地点等要素。

3. **模型应用**
   - 基于大语言模型组织任务逻辑并定义任务指令。
   - 对数据进行需求识别与要素抽取。

#### 潜在研究话题总结

1. **救助需求特征分析**
   - 分析不同类别需求的主体、内容及地点分布特征。
   - 探讨需求要素之间的关联关系。

2. **需求演化规律**
   - 分析需求在事件发展的不同阶段的变化趋势。
   - 探索需求分布的时空规律。

3. **基于大语言模型的需求挖掘优化**
   - 评估大语言模型在救助需求识别与要素抽取中的表现。
   - 探索任务逻辑与指令设计对模型性能的影响。

4. **社交媒体在灾害应急管理中的作用**
   - 探讨社交媒体在突发灾害中的信息传播与资源协调作用。
   - 分析救助需求与舆情讨论之间的关系。

5. **政策优化与建议**
   - 根据需求分析结果，提出针对自然灾害应急管理的政策优化建议。
   - 探讨如何提升救助行动的效率与精准度。

该数据集为研究社交媒体在自然灾害救助中的应用提供了丰富的分析素材，同时为优化救助需求挖掘技术与提升应急管理效率提供了重要支撑。



### 科学极化数据集-新冠肺炎感染后遗症
本数据源自2019级信息资源管理专业本科毕业论文《网络社交媒体中的科学极化现象——以新冠肺炎后遗症为例》，毕业生张天题。
#### 数据背景

本研究的数据集来源于新浪微博，围绕“新冠肺炎感染后遗症”话题展开分析，重点在于挖掘公众对新冠后遗症的观点分布和传播机制。研究选择2022年12月1日至2023年3月1日期间的微博内容，以捕捉在该时间范围内观点极化形成的动态。

#### 数据集的数量

1. **初步数据**
   - 选取相关关键词后筛选出讨论量最高的内容。
   - 按转发、点赞、评论数降序排列，选取排名前1000的微博。

2. **研究用户数据**
   - 从1000篇文章中选取150位不重复的博主。
   - 包括：
     - 官方媒体/组织：12位。
     - 微博认证用户：55位。
     - 普通用户：83位。

3. **用户态度分类**
   - 中立/客观态度：34位。
   - 认为后遗症严重：67位。
   - 认为后遗症影响轻微：49位。

#### 数据集包含的具体维度与字段

1. **微博博文字段**
   - `user_id`：用户ID。
   - `content`：推文内容。
   - `likes_count`：点赞数。
   - `comments_count`：评论数。
   - `reposts_count`：转发数。
   - `identity_info`：用户身份信息（普通用户、认证用户、官方媒体）。

2. **用户社交关系字段**
   - `followers`：关注列表。
   - `retweets`：转发关系。
   - `likes`：点赞关系。

3. **态度标注字段**
   - `attitude`：用户态度，分为0（中立）、1（严重后遗症）和2（轻微影响）。

#### 数据预处理与网络模型构建

1. **数据预处理**
   - 根据互动数据（转发、点赞、评论）计算用户影响力，筛选出代表性博文和用户。
   - 爬取用户的关注列表和互动数据。

2. **网络模型构建**
   - 节点：选择150个用户作为网络节点。
   - 边缘：基于用户间的关注关系、转发关系、点赞关系。
   - 工具：使用Ucinet软件构建整体与子群网络图谱。
   - 标记用户态度：
     - 中立态度用户标记为0。
     - 认为后遗症严重的用户标记为1。
     - 认为影响较轻的用户标记为2。

#### 潜在研究话题总结

1. **观点极化形成机制**
   - 分析用户在新冠后遗症话题上的观点如何极化，并探讨影响因素。

2. **信息传播路径与动力学**
   - 研究社交关系网络中的信息传播速度、范围与动力机制。

3. **用户身份与观点的关联性**
   - 探讨不同身份用户（普通用户、认证用户、官方媒体）的观点分布差异及影响因素。

4. **态度与互动行为的关系**
   - 研究用户在不同态度分类下的互动特征（点赞、评论、转发等）。

5. **舆情演化与热点分析**
   - 基于时间维度分析新冠后遗症相关舆情的演化趋势及热点事件。

6. **社交网络对舆论的放大作用**
   - 探讨社交网络结构如何影响舆论的传播与放大效应。

通过上述分析，该数据集为理解新冠后遗症舆情动态及传播机制提供了重要支持，并为公共健康政策沟通策略的优化提供参考。




### 《辛德勒的名单》影评数据
本数据源自2020级信息资源管理专业本科毕业论文《突发事件下的网络舆情演变分析——以《辛德勒的名单》影评为例》，毕业生林轶航。
#### 数据集的基本内容与背景
- **研究背景**：本数据集以巴以冲突为背景，旨在探讨电影《辛德勒的名单》的影评在突发事件中的网络舆情演变。
- **数据来源**：数据主要来自豆瓣和哔哩哔哩两个平台。
  - **豆瓣**：以“豆瓣电影”模块的短评、影评和小组讨论为主。
  - **哔哩哔哩**：包括官方播放渠道的评论和用户二次创作内容的评论。

#### 数据集的数量
- 初步清洗后的数据总量为 **13,227 条**。
- 经过进一步筛选后，最终有效数据为 **9,440 条**。
- 数据划分为以下五类：
  1. **豆瓣短影评**：2,282 条。
  2. **豆瓣长影评**：2,682 条。
  3. **豆瓣讨论区**：3,430 条。
  4. **哔哩哔哩官方播放渠道评论（根回复）**：953 条。
  5. **哔哩哔哩子回复及二创视频评论**：3,880 条。

#### 数据集包含的具体维度
- **用户ID**：唯一标识用户。
- **评论时间**：评论的具体时间。
- **评论内容**：文本主体。
- **点赞数**：用户对评论的支持度。
- **电影评分**：用户对电影的评价（部分数据包含）。
- **评论结构**：如“话题-回复-子回复”的层次结构。

#### 数据集的潜在研究话题
1. **舆情主题演变**：结合LDA主题模型，探讨影评从电影内容转向对巴以冲突的关注，及其背后的演变规律。
2. **情感分析**：分析用户在不同阶段对影片的情感表达（正向、负向及细粒度分类）。
3. **评论互动性的影响**：研究讨论区与影评区中用户互动行为如何影响舆情主题的变化。
4. **评论字数限制的影响**：分析评论字数限制对主题深度及情感表达的约束作用。
5. **平台间差异**：比较豆瓣和哔哩哔哩在影评舆情数据中的表现差异。

总结来看，这一数据集为分析突发事件背景下的网络舆情变化提供了丰富的文本语料和多样化的分析维度，同时为进一步研究舆情演变机制和对策提供了数据支撑。

### “新冠后遗症”舆情数据集
本数据源自2020级信息资源管理专业本科毕业论文《网络社区用户群体极化的类型演变现象研究：以对新冠后遗症的讨论为例》，毕业生董展辰。
#### 数据集背景
- **研究主题**：探讨在Bilibili平台关于“新冠”和“后遗症”的视频评论内容，分析公众对新冠后遗症的关注与讨论。
- **数据来源**：通过在Bilibili平台检索关键词“新冠”和“后遗症”获取评论数据。
- **采集工具**：使用EasySpider软件进行数据采集。

#### 数据集数量
- **原始数据量**：共采集到 **51,807 条**评论。
- **筛选后数据量**：经过BERT模型筛选后，保留 **7,989 条**与“新冠后遗症”相关的有效评论。

#### 数据处理与筛选
- **无关数据剔除**：
  - 删除无意义或与主题无关的评论（如“沙发”“希望新冠成为过去式”）。
- **模型筛选**：
  - 使用BERT模型（bert-base-chinese）对评论文本进行分类。
  - **人工标注**：随机抽取2,000条评论进行人工标注（与“新冠后遗症”相关标记为1，否则为0）。
  - **训练集与测试集划分**：以9:1的比例划分标注数据，用于模型微调。
  - **模型性能**：经过五轮训练，模型在测试集上的准确率稳定在85%。
  - **结果检验**：从筛选出的7,989条有效数据中随机抽取100条人工检验，相关性为96%，验证清洗效果较好。

#### 数据包含的具体维度与字段
- **评论文本**：用户评论内容。
- **模型判断标签**：是否与“新冠后遗症”话题相关（1为相关，0为无关）。
- **人工标注结果**（用于模型训练与评估）。

#### 数据集潜在研究话题
1. **公众对新冠后遗症的关注热点**：
   - 通过高频词分析，挖掘网民在讨论新冠后遗症时的主要关注点（如症状、治疗、康复经验等）。
2. **情感分析**：
   - 分析公众在讨论新冠后遗症时的情感倾向（如焦虑、乐观、担忧）。
3. **舆情传播特性**：
   - 探讨在Bilibili平台，评论内容的热度（如点赞量、回复量）如何影响话题传播。
4. **模型筛选的局限性**：
   - 研究语言模型在处理涉及医疗健康领域的复杂表达时的有效性与挑战。
5. **后遗症讨论的区域或群体特性**：
   - 如果能获取评论者背景信息，可进一步分析不同地区或群体对后遗症讨论的差异。

通过筛选后的数据集为深入研究新冠后遗症相关的公众讨论与舆情特性提供了良好的基础，同时体现了人工标注与语言模型结合的高效筛选能力。

### 社交媒体谣言识别数据
本数据源自2018级信息资源管理专业本科毕业论文《基于特征分析的社交网络谣言识别研究》，毕业生俞果。
#### 数据背景

本研究基于新浪微博不实信息举报平台的中文谣言数据集展开分析，旨在构建和优化自动谣言检测模型，并提升模型的可解释性。
- **数据来源**：新浪微博不实信息举报平台。
- **研究背景**：刘知远等在《中文社交媒体谣言统计语义分析》中提出的数据集首次面向中文社交媒体进行大规模定量研究，并提出自动辟谣框架，但未深入分析各类特征对模型的贡献度及可解释性。

#### 数据集的数量

1. **初始数据集**：
   - 谣言数据：1,538条。
   - 非谣言数据：1,849条。
   - 总计：3,387条。

2. **最终研究数据集**：
   - 谣言数据：1,318条（去除未标识真实性的数据后）。
   - 非谣言数据：1,840条。
   - 总计：3,158条。

3. **扩展数据集（CED_Dataset）**：
   - 包含转发与评论信息，数据量为31,669条。

#### 数据集包含的具体维度与字段

1. **核心字段**
   - `rumorCode`：谣言的唯一编码。
   - `title`：被举报的谣言标题。
   - `informerName`：举报者的微博名称。
   - `informerUrl`：举报者的微博链接。
   - `rumormongerName`：发布谣言者的微博名称。
   - `rumormongerUrl`：发布谣言者的微博链接。
   - `rumorText`：谣言内容。
   - `visitTimes`：谣言被访问次数。
   - `result`：谣言审查结果。
   - `publishTime`：谣言的发布时间。

2. **数据预处理字段**
   - `seg`：分词结果。
   - `stop`：去除停用词后的文本。

#### 数据预处理

1. **数据清洗**
   - 去除未标识真实性的数据。
   - 删除对模型训练无意义的词语，如“的”、“了”、“呢”等。

2. **分词处理**
   - 使用jieba分词包将文本分词，并将高关联概率的汉字组成词组。

3. **特征构建**
   - 为LDA主题分析及其他语言模型的构建奠定基础。

#### 潜在研究话题总结

1. **自动谣言检测模型构建**
   - 探索如何利用特征工程和深度学习技术（如BERT、SVM）优化谣言检测模型。

2. **模型可解释性研究**
   - 分析不同特征对谣言识别模型的贡献度，提升模型的可解释性。

3. **谣言传播路径与行为分析**
   - 利用扩展数据集（CED_Dataset）中的转发与评论信息，研究谣言传播的路径与用户行为模式。

4. **语义与时序分析**
   - 结合文本语义特征与时间序列特征，研究谣言传播的时空规律。

5. **数据集扩展与多领域应用**
   - 将谣言检测技术推广至其他领域（如健康、政治等），探索跨领域谣言检测的通用性。

6. **对比研究**
   - 对比基于中文社交媒体的数据与其他语言和平台上的谣言数据集，研究跨文化、跨平台的谣言特征。

该数据集为深入研究中文谣言检测和传播规律提供了坚实的数据基础，同时为探索模型优化和应用场景扩展提供了广阔空间。

### 社交媒体政治极化数据
本数据源自2020级信息资源管理专业硕士研究生毕业论文《用户立场视角下的社交媒体群体极化：基于深度学习的分析》，毕业生汪子航。
#### 数据背景

本研究聚焦美国公共事件中的公众舆论立场与演化，以2023年4月5日美国前总统唐纳德·特朗普被拘捕事件为切入点，收集Twitter和YouTube上的相关讨论数据。通过分析社交媒体用户对该事件的立场分布和互动特性，探讨大型公共事件对公众态度和社交媒体舆论的影响。

- **事件背景**：
  - 2023年4月5日，特朗普成为美国历史上首位被刑事起诉的前总统。
  - 事件引发了公众在社交媒体上的广泛讨论，凸显了美国政治与民意撕裂。

#### 数据集的数量

1. **Twitter数据集**
   - **推文数量**：8条推文。
   - **回复数量**：共收集199,613条推文回复。

2. **YouTube数据集**
   - **视频数量**：146条相关视频。
   - **评论数量**：共收集197,918条视频评论。

#### 数据集包含的具体维度与字段

1. **Twitter数据字段**（表3.5）
   - `tweet_id`：推文ID。
   - `date`：推文发布时间。
   - `text`：推文文本内容。
   - `name`：发布者网名。
   - `username`：发布者用户名。
   - `userid`：发布者用户ID。
   - `in_reply_to_tweet_id`：回复对象推文ID。
   - `in_reply_to_username`：回复对象用户名。
   - `in_reply_to_userid`：回复对象用户ID。
   - `language`：语言。
   - `quote_count`：引用次数。
   - `retweet_count`：转帖次数。
   - `reply_count`：回复次数。
   - `like_count`：点赞次数。
   - `user_verified`：用户是否认证。
   - `user_verified_type`：用户认证类型。
   - `user_location`：用户位置。
   - `user_created_at`：用户注册日期。
   - `user_description`：用户个人描述。
   - `user_followers_count`：用户粉丝数量。
   - `user_following_count`：用户关注数量。
   - `user_tweet_count`：用户推文数量。

2. **YouTube数据字段**（表3.7）
   - `author`：发布者用户名。
   - `id`：评论ID。
   - `parent`：上级评论的ID。
   - `publishtime`：评论发布时间。
   - `likeCount`：点赞次数。
   - `comment`：评论文本。

#### 数据预处理

1. **Twitter数据预处理**
   - 使用高级检索功能筛选关键词“Trump”，筛选回复数量大于20,000的推文。
   - 补充右倾与左倾用户的推文数据以平衡样本。
   - 收集推文下的所有回复数据，包括互动信息（点赞、转发、回复数量）与用户信息。

2. **YouTube数据预处理**
   - 使用关键词“Trump”+“arrest”和“Trump”+“arraign”筛选相关视频。
   - 对关闭评论区的视频予以排除。
   - 收集视频评论，并统计评论数量分布。
   - 未收集普通用户的个人信息，仅提取有效评论内容及互动数据。

#### 潜在研究话题总结

1. **公众立场分析**
   - 探索在特朗普被拘捕事件中，美国公众在社交媒体上的立场分布及其背后的驱动因素。

2. **舆论传播路径与特征**
   - 研究Twitter和YouTube上关于特朗普事件的舆论传播路径及互动特征。

3. **左右立场舆论比较**
   - 对比左倾与右倾用户在讨论该事件时的行为模式和立场表达。

4. **平台间传播差异**
   - 比较Twitter与YouTube平台在信息传播范围、深度及互动性上的差异。

5. **高互动内容分析**
   - 分析回复数和评论数较高的内容特征，探索高互动舆论内容的构成及影响力。

6. **政治事件与社交媒体舆论动态**
   - 探讨重大公共事件如何通过社交媒体加深或缓和公众的政治分裂。

该数据集为理解美国大型公共事件中的公众舆论态势与传播规律提供了丰富的研究基础，具有重要的社会学与传播学研究价值。

