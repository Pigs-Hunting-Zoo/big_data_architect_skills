----- 还未完成 持续更新中 
# 大数据架构师该掌握的技能
主要分为两块 <a href="#硬能力">硬能力</a> 与 <a href="#软实力">软实力</a>  
>  
## <a name="硬能力">硬能力</a>
 
 - 一：平台建设
   - 1.行业平台
     - 1）大平台
         - <a href="https://cloud.google.com/">谷歌云</a>
         - 亚马逊云
         - 阿里云
         - 腾讯云
         - 网易云
         - 华为云
     - 2）小平台
         - 国云
         - 国双
         - 青云
         - 勤思
     - 3）专业工具平台
         - <a href="https://www.bdp.cn/home.html">海致BDP</a>
         - <a href="http://www.yonghongtech.com/">永洪</a>
         - <a href="https://www.analysys.cn/">易观</a>
     - 4）APP分析平台
         - <a href="https://mixpanel.com/">mix panel</a>
         - <a href="https://www.growingio.com/">growing IO</a>
         - <a href="http://www.sensorsdata.cn/">神策</a>
         - <a href="https://zhugeio.com/">诸葛 IO</a>
   - 2.技术选型
     - 1）<a href="https://www.cloudera.com/products/open-source/apache-hadoop/key-cdh-components.html" >CDH</a>
     - 2）<a href="https://hortonworks.com/products/">HDP+HDF</a>
     - 3）<a href="https://mapr.com/">MAPR</a>
     - 4）<a href="http://www.transwarp.cn/">Transwarp</a> 
   - 3.平台架构
     - 1）HDP Core(平台核心也是Hadoop core)
         - HDFS(存储)
         - MapReduce(批处理)
         - Yarn(基础资源调度)
             - 负责集群资源的统一管理和调度
             - 单节点资源管理和使用 
             - 应用程序管理 
             - 对任务运行环境的抽象 
             - 支持运行长应用程序和短应用程序
             - 支持docker fpga
             - 期待更细粒度的资源控制
             - 对比Mesos
         - Oozie(任务调度编排)
             - 平台调度的基础保障
             - hadoop 各种任务的使用与调度
             - 对比 Azkaban Airflow 
         - Slider(调度支持 新版已经集成yarn)
     - 2）Enterpise Data Warehouse(企业数据仓库)
         - Pig(基础脚本服务)
             - 用类sql语言保证mr执行顺畅
             - pig latin 的执行环境 
         - Hive(数据仓库存储)
             - 基础数据仓库(ods gdm dw app dim)
             - 基础ETL的运行实例
             - OLAP的数据存储(kylin)
             - 各种数据的hive外表用于查询
             - 对比presto impala hawq 
         - Druid(adhoc方案 实时多维查询和分析)
             - 已处理数十亿事件和TB级数据
             - 实时查询分析 高可用、高容错、高性能
             - 交互式聚合和快速探究大量数据
             - 为OLAP工作流的探索性分析而构建，支持各种过滤、聚合和查询
             - 对比 drill es mdrill  等
         - Tez(简化增强hive)
         - Sqoop(数据导入导出工具)
     - 3）Data sclence(数据科学)
         - Spark(内存通用并行计算)
             - 推荐相关
             - 数据清洗
             - 特征抽取
             - 预测相关
             - 对比 flink storm
         - Spark sql(结构化数据处理) 
         - Spark streaming(spark流式处理)
         - Zeppelin(界面分析挖掘工具)
             - 基于R和python的单机界面使用工具(分析挖掘)
             - 基于spark kafka 的界面操作工具
             - 基于预测数据的使用与展现
             - 支持pandas numpy
             - 支持R 
             - 支持hive  hbase spark sparksql sparkstreaming
             - 支持keras matplotlib pysql
     - 4）Operational data store(操作KV存储)
         - Hbase(kv数据存储)
         - Phoenix(hbase 类sql查询)
     - 5）Securlty governance(安全治理)
         - Knox(鉴权工具)
             - 数据的权限鉴权通道
             - 平台跟外部的出入口 
         - Ranger(权限管理工具)
             - 架构下各组件的权限管理
             - 记录操作日志到solr 
         - Atlas(元数据溯源与数据治理工具)
             - 大数据平台下各种操作的元数据记录
             - 数据打标签(对于维度 指标 ETL等)
             - 可查询hive storm spark sqoop oozie nifi 元数据，可自定义实现自己的需要查看和维护的工具
             - 数据流转流程的图像化展现
             - 元数据操作记录与各种信息查询 
     - 6）Stream procressing(流式计算)
         - Storm(实时数据处理分析)
         - Kafka(数据消息队列)
         - <a href="https://hortonworks.com/open-source/streaming-analytics-manager/">Streaming Analytics Manager	(流式数据处理界面工具) </a>
             - 拖放可视化设计，开发，部署和管理流式数据分析应用程序
             - 进行事件关联，上下文衔接，复杂模式匹配，分析聚合以及创建警报/通知 
         - MiNiFi(边缘数据处理)
             - 数据产生的源头收集和处理数据
             - 通过实现边缘设备智能(edge intelligence)来调整数据流的双向通信
             - 可以数据溯源(Data Provenance)
             - 可以集中管理和下发Agents
             - java agent
             - c++ agent 
     - 7）Operations(平台运维工具)
         - Ambari(大数据平台管理工具)
         - Ambari Metrics(监控平台各类服务及主机的运行情况)
         - Ambari Infra
         - Zookeeper(基础分布式保证工具)
         - Solr(搜索应用 操作日志存储)
     - 8）Data operation platform(数据操作平台)
         - NiFi(数据 ETL 数据流处理)
             - 日志清洗 业务数据入库
             - 基础数据(mysql binlog业务库 )ETL
             - 部分外部数据
             - 自定义数据接入方式
             - 自定义数据流程处理
             - 数据输出出口
         - NiFi Registry(NiFi版本管理工具)
             - NIFI的版本记录回溯
             - NIFI Schema Registry 来统一文件定义(类配置中心) 
             - 配合SwaggerAPI数据定义 
         - Hue(大数据交互界面平台)
     - 9）Data visualization(数据可视化工具)
         - Superset(数据分析界面工具)
         - <a href="http://www.finebi.com/product/">FineBI(BI界面分析工具)</a>
             - 报表数据可视化
             - 部分OLAP分析
             - Fine Index
             - FIne Direct
             - 现场数据实时展示 
         - <a href="https://tuiqiao.github.io/CBoardDoc/#/">(Cboard) 主用于数据导出</a>
         - <a href="http://metabase.com/" >Metabase</a>
             - 直接用来对接运营产品的数据交互工具
             - 支持问题模式,支持对数据进行标记 
         - 对比 Saiku Tableau Qlikview 
         - 自主研发
             - Echarts
             - inMap 
     - 10）Kylin(MOLAP数据分析工具)
   - 4.资源申请
     - 1）基准测试
     - 2）资源预估(基于业务存量与增量)
     - 3）理解各组件的CPU IO 内存 硬盘 带宽的特性
     - 4）瓶颈资源预判
     - 5）分阶段保障 
   - 5.日常维护
     - 1）bigdata devops
     - 2）权限授权
     - 3）瓶颈判断
     - 4）继续需求的二次开发
     - 5）组件版本关注与升级
     - 6）各种疑难杂症修复
     - 7）环境维护(正式 测试)
   - 6.技术调研 
     - 1）图数据库
         - Janus Graph
         - Dgraph
         - Neo4j
         - ArangoDB
     - 2）机器学习
     - 3）IOT相关
     - 4）边缘计算
   - 7.云平台化建设  
 - 二：数据获取
   - 1.公司内结构化数据
     - 1）增量
     - 2）全量
     - 3）拉链
     - 4）binlog
     - 5）接口
   - 2.公司内非结构化数据
     - 1）日志
         - 接口
         - 内部埋点
             - 后端埋点方案
             - 无埋点方案
             - url规约系统
             - 用户级别
             - 页面级别
             - CMS块级别
             - 事件级别
         - 第三方埋点
             - GA
             - 百度
             - 友盟
             - 其他
         - 搜索
     - 2）视频
     - 3）图像
     - 4）excel
     - 5）文档
   - 3.外部数据(非公司IT支撑)
     - 1）爬虫平台开发利用推进
     - 2）API对接
     - 3）销售使用的外部工具数据取回
         - <a href="http://www.qixin.com/">启信宝</a>
         - <a href="https://www.qichacha.com/">企查查</a>
         - <a href="https://www.tianyancha.com/">天眼查</a>
         - <a href="https://www.foxsaas.com/">赤狐</a>
         - 各种CRM
     - 4）运营使用的外部工具数据取回
         - <a href="http://e.qq.com/ads/" >广点通</a>
         - <a href="http://dmp.taobao.com/" >达摩盘</a>
         - 知乎DSP
         - <a href="https://ad.toutiao.com/">今日头条系</a>
         - <a href="https://mtj.baidu.com/web/welcome/login">百度系</a>
         - <a href="https://weibo.com/">微博营销工具</a> 
         - <a href="https://dev.getui.com/dev/#/login">个推</a>
         - 腾讯信鸽
         - 各种统计平台
         - ......
   - 4.外部数据
     - 1）数据报告
         - <a href="http://www.199it.com/archives/category/report">199IT(100+)</a>
         - <a href="http://report.iresearch.cn/">艾瑞(100+)</a>
         - <a href="https://detail.youzan.com/show/goods/newest?alias=2xlainh68rpkq">IT橘子</a>
         - <a href="http://www.cnnic.net.cn/hlwfzyj/hlwxzbg/">国家互联网中心</a>
         - 恒大研究院
         - <a href="https://www.iyiou.com/intelligence/resource/ ">亿欧智库</a>
         - <a href="https://www.analysys.cn/article#analysis">易观数据</a>
         - <a href="http://www.catr.cn/kxyj/qwfb/bps/">中国通信研究院</a>
         - <a href="https://e.tencent.com/v2/report/datareport.php">腾讯数据实验室</a>
         - <a href="http://www.aliresearch.com/blog/index/lists/tag/3831.html">阿里研究中心 </a>
     - 2）商业合作
         - 数据交换
         - 专项购买
         - 流量互补 
     - 3）竞品数据
         - 分析竞品列表
         - 爬虫获取商家 商品 评论等业务数据
         - 从一些公开平台获取统计数据
     - 4）行业数据
         - 大盘数据
         - 行业动态数据 
     - 5）统计数据
         -  <a href="https://account.similarweb.com/">Similar web</a>
         -  <a href="https://www.newrank.cn/">新榜</a>
     - 6）数据资讯
         - <a href="http://zhidx.com/">智东西</a>
         - <a href="http://hao.199it.com/">大数据导航</a> 
 - 三：数据价值
   - 1.数据清洗
     - 日志数据清洗(UDF SparkStreaming )
     - 业务数据清洗
     - 维度数据抽取
     - NLP语义化
     - 图片识别等
   - 2.数据仓库
     - 1）分层
         - Operational Data Store(ODS) 原始操作数据
         - General Data Mart(GDM)清洗后通用数据
         - Data WareHouse	(DW)数据集市
         - Dimension Data(DIM)维度数据
     - 2）规范
         - 权限规范
         - ETL规范
         - 调度规范
     - 3）ETL
     - 4）元数据(Atlas查看和标记)
         - 业务元数据
         - ETL元数据
         - 数据元数据 
   - 3.统计报表
     - 分类
     - 维度
     - 指标
     - 数据可视化
   - 4.商业智能
     - 关键指标与转化
         - 博弈分析法(找到博弈方，找到博弈方的冲突与矛盾)
         - 企业价值评估法(找到利益保持或者增长的关键点或者业务流程量化KPI)
         - 行业参考(标准行业的指标体系)
     - 影响业务决策
     - 影响运营决策
     - 影响老板决策 
   - 5.数据报告
     - 抓重点业务或关键路径
     - 体系化叙述
     - 重点数据解释
     - 编写参考 玩转keynote
   - 6.业务赋能
     - 用户画像
     - 推荐
     - 广告
     - 数据预警
     - 数据预测
     - 数据查询
     - 对运营支持的数据工具
     - 对业务销售支持的数据工具
   - 7.数据产品
     - 2B
     - 2C
   - 8.场景探索 
 - 四：数据安全
   - 1.企业数据分级
     - 普通
     - 敏感
     - 机密
     - 绝密
   - 2.数据隐私保护
     - Personal Identifiable Information(PII级别)
     - 用户唯一标识(因公司而异)
     - 核心业务数据订单 优惠券 等(掩码) 
   - 3.平台权限控制
     - 数据导出权限控制
     - 账号跟踪与密钥更换
     - 数据使用申请
   - 4.数据流程规范
     - 需求对接规范
     - 数据订正规范
     - 业务数据变更修正
 - 五：质量保障
   - 1.平台与资源保障
   - 2.数据质量
   - 3.统一口径
   - 4.故障跟进
 
>
## <a name="软实力">软实力</a>

 - 一：个人素质
   - 1.体系化建设
     - 1）快速了解一个体系
         - 渠道
             - 专业图书
             - 技术官网
             - github
             - <a href="https://www.processon.com/popular">processon 里的推荐功能</a>
             - 技术博客
             - 知乎
             - 体系报告网站(参考 数据获取-外部数据-数据报告)
             - 各种行业平台网站
             - 谷歌百度
             - 找朋友聊  加微信QQ群
         - 记录整理
             - 找个工具记录 散漫的疯狂阅读与吸取
             - 最好用表格来划分横向维度和纵向维度
         - 消除杂音  
             - 刨除过程中一些过时的资料或者概念
             - 尽量找原版的设计与理解
     - 2）快速形成自己的理解(就像我整理这个脑图一样)
         - 聚合
         - 分类
         - 排序
         - 深入
     - 3）系统计划
     - 4）修正策略 
   - 2.业务破局
     - 1）了解业务
         - 老板 高管 经理
             - 投其所好
                 - 多渠道的了解老板画像
                 - 试探数据价值的关注度 
             - 换位思考
                 - 从他们的角度去考虑他们遇到的困难，不解和所做的决定
                 - 不要被他们的思维固化(在其位谋其政)影响你对于数据价值的思考 
             - 全面的体系 重要的分级
                 - 全面的体系化建设(基于对行业 业务 数据 的宽泛认知) 
                 - 永远要记住摸清主线
                 - 按照重要程度(看势)做事情的分级
             - 观察对方的底线(长期) 
         - 技术 产品 运营
             - 技术体系初步印象
                 - 前端(ios android pc tv) 涉及到埋点日志事情
                 - 后端(微服务 链路 数据库) 涉及到业务数据入库和日志收集
             - 掌握全局(局部)数据库
                 - 先全面后局部的感觉下数据库设计(如果有ER图提供最好)
                 - 感觉下量级与增速
             - 深入了解产品的规划
                 - 找到契合点 不要越界
                 - 数据价值为主 外层的展现为辅
                 - 产品方向的数据价值多数来自C端 所以 推荐 广告  用户画像等为主 不同的行业考虑下特性应用(O2O IOT 新零售 AI的落地应用)
             - 拿出诚意才会得到配合
                 - 站在开发者角度去尽量减轻他们的负担
                 - 日志与埋点的配合
                 - 业务数据入库配合
                 - 底层运维支持配合
                 - 技术层面的分享带给别人更多理解相关技术的机会
             - 是否需要数据产品经理
                 - 涉及到产品规划和业务赋能的最好有数据产品对接
                 - 关于数据报表分析的最好让数据分析人员进入对接一线
         - 销售 业务 财务
             - 良好的沟通从兴趣开始 
             - 数据价值来源于解决B端面临问题
                 - 是否能提供有价值的数据让业务跑得更快
                 - 能否提供销售更直接的客户服务数据
                 - 财务的事情佛系对待
             - 合适的机会跟他们一起开会，反复强调的内容里面就有重点和痛点
             - 多花时间研究他们的工作流程
                 - 流程最能体现价值(优化 提速 转化 效率)
                 - 接触工作流程中可以更深刻的理解业务
             - 关键指标一定会有所提及(不懂找资料学习再沟通) 绕不过的钱
                 - 记录关键指标 自己先琢磨在找懂的人沟通
                 - 遇到不分享的可以先想办法解决他的一些问题，无论大小，展现诚意。记住自己的目标
     - 2）分析痛点
         - 将痛点归类(部门 角色  数据源 数据价值) 
         - 归类后痛点间的关联关系找主线
         - 能解决的痛点才是痛点
         - 缩小范围解决头部需求反手解决次类需求
     - 3）专注行动
         - 象限法(重要紧急四象限)
             - 优先处理 重要且紧急 紧急不重要的
             - 阶段性的处理重要不紧急的(这种事情要记录在本本上) 
         - 行动前的影响与价值预估
             - 可能对其他部门或人造成的工作加重减轻与正负面影响
             - 行动能得到的可能价值(对需求方 相关人 团队 自己)
         - 可拆解的任务才能行动
             - 行动计划保证在一个可控范围内(人员 时间 资源 )
             - 任务的串并行尝试
             - 人员维度的安排
             - 时间维度的安排
         - 行动中的修正与反馈
             - 寻找一个反馈对象(最好是需求方)
             - 修正来源于对结果的不可控(保证损失最小)
         - 拿到结果一定要说话(不要当哑巴 付出得到回报天经地义)
             - 打算说给谁听
             - 准备好PPT(参见玩转keynote)
             - 时间地点
   - 3.数据解读
     - 1）考虑受众
     - 2）实事求是 轻易不下结论
     - 3）多维度解读 
   - 4.工具利用
     - 1）时间管理工具
         - <a href="https://www.omnigroup.com/omnifocus/">Omni Focus </a>
         - <a href="https://www.tyme-app.com/">Tyme2</a>
     - 2）快速记录工具
         - 备忘录
         - Wiki
         - <a href="http://macdown.uranusjr.com/">Macdown</a> 
     - 3）扩展思维工具
         - <a href="https://mindnode.com/">MindNode</a>
         - <a href="https://www.processon.com/">Processon</a>
     - 4）学习成长工具 
   - 5.清醒复盘
     - 1）复盘前的思考
     - 2）何时复盘
     - 3）避坑总结
   - 6.玩转keynote
     - 1）确定主题与讲述思路
         - 解决痛点模式
         - 突出主题模式
         - 流程讲解模式
         - 技术分享模式
         - 融资招商模式
         - 数据报告模式
     - 2）讲述靠说不靠堆叠
         - 言简意赅
         - 归纳总结
     - 3）利用模板来快速制作和辅助思路
         - 参考模板
             - <a href="https://share.weiyun.com/04bb12cb3f5a8172d38d3794bac5bf4e">Layouts for Keynote(App Store有售)</a>
             -  <a href="http://www.pc6.com/mach/macmuban/" >PC6合集</a> 
         - 辅助思路
             - 当有些思路阻碍可以看看模板上被人是如何处理和展现的
             - 运用模板的特殊元素来装扮自己的文案
     - 4）基础色调选取与排版建议
         - 色调选择
             - 运用模板的特殊元素来装扮自己的文案
             - 多用过度色 原则上整体别超过5个
             - 颜色可以用吸管 从浅入深或由深入浅波动选择
             - 黑白灰为常用过度配色
             - 分清极暖色 极冷色 暖色 冷色 微暖 微冷
             - 色彩的对比 平衡 混合  多练习
         - 排版建议
             - 建议用“细黑”的字体，比如冬青黑体，华文雅黑，微软雅黑light等
             - 节奏感：尺寸大小，上下位移，旋转，间距，就是不能让文字之间稳当地排在一起
             - 巧用各种图形 可以更形象化的让人理解
             - 大纲最好列在每页的面包屑上
         - 巧用动画
   - 7.行业关注
 - 二：团队管理
   - 1.遇见对的人
   - 2.人尽其才
     - 组团队
     - 差异化
     - 重培养 
   - 3.上通下达
   - 4.拒绝沉溺(不要给鱼)
   - 5.老司机别翻车
       - 容忍与控制
       - 不要触碰底线
       - 没有什么是烧烤不能解决的 如果有那就两顿
 - 三：技术能力 
   - 1.编程
   - 2.算法
   - 3.数据仓库
   - 4.工程
 - 四：人生之路
   - 1.平衡之道
     - 1) 规划VS变动
     - 2) 领导VS下属
     - 3) 个人VS团队
     - 4) 资源VS价值
     - 5) 家庭VS工作
   - 2.破除心魔
     - 1）以结果导向
	      - 理论上个人感受会是结果导向的障碍
	      - 结果是个大家相对一致的预期结果
	  - 2）接受一家公司代表要融入一种文化
	      - 是否喜欢是个很重要的分水岭
	      - 无论什么企业文化都会以结果为导向
	      - 综合评定自己的容忍度
	  - 3）敲碎or划清边界
	      - 阻碍目标的大多都是边界内自己要做或者推动的 
	  - 4）多维度的看待事情
	      - 不要再不同纬度观点下讨论事情，这样容易产生无谓的争执
	      - 当一种角度理解不了某些人或事的时候那就切换下角度
	      - 对一个事情或者一个人的评判一定不要单纯的一个角度下结论
	      - 同样的维度之间切换自如有助于你讨喜
	  - 5）信任之路且行且珍惜
	  - 6）道德沦陷还是底线失守
	      - 改变自己，做自己认为恶心的事情是不是就是道德沦陷
	      - 底线是一个恒久不变的还是一个根据自己的发展阶段 家人 事业 朋友动态调整的 
   - 3.推荐书籍
     - 1）技术类(不包含理论与技术框架)
         - 《数学之美》
         - 《数据仓库工具箱：维度建模的完全指南》
         - 《美团机器学习实践》
         - 《数据挖掘与数据化运营实战 思路、方法、技巧与应用》
	  - 2）业务类
	      - 《无印良品的改革》
	      - 《增长黑客》
	      - 《智联网》
	      - 《浪潮之巅》
	      - 《京东平台化数据运营》
	  - 3）管理与心理学
	      - 《原则》
	      - 《乌合之众》
	      - 《说谎》
	      - 《卓有成效的管理者》
	      - 《九型人格》
	      - 《影响力》

# 技能图
![](img/大数据架构师该做到的.jpg)
