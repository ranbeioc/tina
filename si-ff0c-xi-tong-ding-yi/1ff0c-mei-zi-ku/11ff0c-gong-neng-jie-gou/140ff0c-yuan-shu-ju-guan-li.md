# 条目元数据管理

即有关原始曲目的信息结构类型数据的增删改查管理。对条目名称别名，多关联角色标记，栏目板块信息的增删改查处理。同时扩充对专辑和歌单和周边类数据的支持。

### 曲库核心标准数据与要求如下：

| 数据字段 | 使用示例与规格 | 所属对象 | 阶段 |
| :--- | :--- | :--- | :--- |
| 编码格式 | UTF-8，GB18030 | 字符集规范 | P1 |
| 防盗链验证 | Y/N | 白名单，域名/地区/平台/版本 | P2 |
| 原始创建时间 | 2017-04-15 01:15:43 |  | P1 |
| 最后更新时间 | 2017-05-15 01:15:46 |  | P1 |
| 最后缓存更新时间 | 2017-06-15 01:15:51 |  | P1 |
|  |  |  |  |
| **曲目（Song）** |  |  |  |
| 曲目编号 | T1234567890 | （唯一标识） | P1 |
| 原文件名 | S1234567890 | 合名（唯一性） | P1 |
| MD5 | 11AFAD2D3555EAB7F251A05C0B7915F9 | 散列函数（资源文件校验） | P2 |
| SHA1 | A48A9D261882A3AF795E4A9CECC47E8EA098EA7E | 数字签名（资源文件校验） | P2 |
| CRC32 | 5DB7252F | 循环冗余效验程序库（资源文件校验） | P2 |
| 歌曲名 | First Love，笨小孩 |  | P1 |
| 演唱类型 | 国/合/演/消/Remix/Live |  | P1 |
| 歌曲封面类型 | {S/M/L} | （尺寸规范另述，下同） | P1 |
| 歌曲封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 歌曲中文首字母 | N/A，BXH |  | P1 |
| 歌曲别名 | 初恋，N/A |  | P2 |
| 歌曲别名中文首字母 | CL， N/A |  | P2 |
| 歌曲时长 | 225s |  | P1 |
| 歌曲风格 | &lt;songtagId&gt;流行 |  | P1 |
| 歌曲类型 | MTV |  | P1 |
| 歌曲语言 | 日语/英语、国语/粤语 |  | P1 |
| 关联艺术家 | &lt;artId&gt;Array | **关联类信息** | P1 |
| 关联专辑 | &lt;albumId&gt;Array |  | P2 |
| 关联歌单 | &lt;sheetId&gt;Array |  | P2 |
| 关联资讯 | &lt;infoId&gt;Array |  | P3 |
| 关联歌曲文件地址 | &lt;songUrl&gt;{type}Array | 请求所属歌曲文件列表 | P1 |
| 关联三方资源 | &lt;videoId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 关联翻唱作品 | &lt;ugcId+userId+TopNum&gt;Array |  | P1 |
| 关联话题 | &lt;topicId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 订阅用户总数 | 235 | **用户类信息** | P1 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P1 |
| 分享用户总数 | 98 |  | P1 |
| 分享用户列表 | &lt;userId&gt;Array |  | P1 |
| 用户评论总数 | 687 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 供应商 | &lt;supplierId&gt; |  |  |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P2 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** | P1 |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |
|  |  |  |  |
| **艺术家（Art）** |  |  |  |
| 歌手编号 | K1234567890 | （唯一标识） | P1 |
| 歌手名 | 宇多田光，刘德华 |  | P1 |
| 歌手标签 | &lt;arttagId&gt; |  | P1 |
| 歌手头像类型 | {S/M/L} |  | P1 |
| 歌手头像地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 合唱歌手编号 | N/A，&lt;singerId&gt;柯受良/吴宗宪 | 多人 | P1 |
| 歌手中文首字母 | YDTG，LDH |  | P1 |
| 歌手别名 | Hikaru Utada，Andy |  | P2 |
|  | 宇多田ヒカル/うただ ヒカル |  | P2 |
| 歌手昵称 | ヒッキー/Hikki，华仔 |  | P1 |
| 歌手别名中文首字母 | N/A，HZ |  | P1 |
| 作词 | 宇多田光，刘德华 |  | P2 |
| 作曲 | 宇多田光，高枫 |  | P2 |
| 伴奏 | N/A，N/A |  | P2 |
| 伴舞 | N/A，N/A |  | P2 |
| 歌手生日 | 6-14 |  | P2 |
| 歌手星座 | 白羊座，狮子座 |  | P2 |
| 歌手所获奖项 | 台湾金曲奖最佳男歌手，MTV年度最佳唱片 |  | P3 |
| 歌手风格 | &lt;songtagId&gt;摇滚 |  | P2 |
| 歌手介绍 | &lt;textInfo&gt; |  | P2 |
| 关联专辑 | &lt;albumId&gt;Array | **关联类信息** | P2 |
| 关联歌单 | &lt;sheetId&gt;Array |  | P2 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P1 |
| 关联资讯 | &lt;infoId&gt;Array |  | P3 |
| 关联三方资源 | &lt;videoId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 关联翻唱用户 | &lt;userId&gt;Array |  | P1 |
| 关联话题 | &lt;topicId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 订阅用户总数 | 268 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 658 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P1 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** | P1 |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |
|  |  |  |  |
| **专辑（Album）** |  |  |  |
| 专辑编号 | Z1234567890 | （唯一标识） | P1 |
| 专辑名称 | First Love，笨小孩 |  | P1 |
| 专辑标签 | &lt;songtagId&gt; |  | P1 |
| 专辑封面类型 | {S/M/L} |  | P1 |
| 专辑封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 发行时间 | 1999-3-10，1998-11-1 |  | P2 |
| 发行公司 | EMI，上海音像公司 |  | P2 |
| 专辑介质 | 数字/CD，VCD/DVD，录像带 |  | P2 |
| 条形码 | 2009307450035 |  | P3 |
| ISRC\(中国\) | CNE029838200，N/A |  | P3 |
| 歌曲总数 | 18 |  | P1 |
| 专辑风格 | &lt;tagId&gt;民谣 |  | P1 |
| 专辑语言 | 日语/英语、国语/粤语 |  | P1 |
| 专辑时长 | 56分钟 |  | P1 |
| 专辑所获奖项 | 日本唱片协会、格莱美最佳外语专辑 |  | P3 |
| 专辑介绍 | &lt;textInfo&gt; |  | P2 |
| 关联艺术家 | &lt;artId&gt;Array | **关联类信息** | P1 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P1 |
| 关联资讯 | &lt;infoId&gt;Array |  | P3 |
| 关联三方资源 | &lt;videoId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 订阅用户总数 | 325 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 分享用户总数 | 678 |  | P2 |
| 分享用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 345 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P1 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** |  |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |
|  |  |  |  |
| **歌单（Sheet）** |  |  |  |
| 歌单编号 | D1234567890 | （唯一标识） | P2 |
| 歌单名称 | 遇见薛子谦 |  | P2 |
| 歌单封面类型 | {S/M/L} |  | P2 |
| 歌单封面地址 | &lt;imageUrl&gt;{S} |  | P2 |
| 创建用户 | &lt;usersId&gt; |  | P2 |
| 歌曲总数 | 29 |  | P2 |
| 歌单标签 | &lt;song+diytagId&gt; |  | P2 |
| 歌单介绍 | &lt;textInfo&gt; |  | P2 |
| 关联话题 | &lt;topicId&gt;Array | **关联类信息** | P2 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 用户评论总数 | 367 | **用户类信息** | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 订阅用户总数 | 325 |  | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 分享用户总数 | 354 |  | P2 |
| 分享用户列表 | &lt;userId&gt;Array |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P2 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P2 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** | P1 |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |
|  |  |  |  |
| **栏目（Section）** |  |  |  |
| 栏目编号 | C1234567890 | 唯一标识 | P1 |
| 栏目名称 | K歌之王串烧 |  | P1 |
| 栏目封面类型 | {S/M/L} |  | P1 |
| 栏目封面地址 | &lt;imageUrl&gt;{L} |  | P1 |
| 创建者 | &lt;adminId&gt; |  | P1 |
| 栏目介绍 | &lt;textInfo&gt; |  | P1 |
| 关联内容 | &lt;song/art/album/sheet-Id&gt;Array | **关联类信息** | P1 |
| 开关状态 | Y/N | **业务类信息** | P1 |
| 上下架时间周期 | 2017-04-01 00:00至2017-06-30 23:59 | 自动上下架 | P2 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P2 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** | P1 |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |

### 主要的的管理项和实施目标如下：

| 从属业务 | 业务项 | 功能项 | 实施 | 阶段 |
| :--- | :--- | :--- | :--- | :--- |
| 曲目元数据入库 | 导入新曲目 | 通过后台导入信息表/字段半自动入库 | 由曲库管理员主动批处理，技术员配合 | P1 |
|  |  | 通过后台增量扫描读取已转码新曲目入库 | 由曲库管理员自动批处理信息导入 | P2 |
| 资源加工入库 | 资源转码 | 通过导入原始文件和配置项自动转码生成资源入库 | 由曲库管理员自动批处理信息导入以及在线配置批处理转码资源文件 | P3 |
|  | 画质加工 | 通过原始文件和选择画质滤镜参数自动转换生成资源入库 | 由曲库管理员在线配置批处理优化资源文件 | P3 |
|  | 消音加工 | 通过原始文件和选择消音参数自动转换生成资源入库 | 由曲库管理员在线配置批处理优化资源文件 | P3 |
|  | 歌词编辑 | 通过原始文件和选择歌词通用参数自动转换生成资源入库 | 由曲库管理员在线配置批处理优化资源文件 | P3 |
| 新歌加工入库 | 新歌查询 | 通过定期网络爬虫获取新歌列表比对缺失新歌项 | 由曲库管理员在线配置源站地址，人工审查列表可用曲目 | P2 |
|  |  | 通过爬虫比对缺失新歌项非独有版权可用曲目，并自动提取新歌元数据信息和原始媒体文件 | 由曲库管理员在线配置源站地址确认最终信息资源后自动入库 | P3 |
|  | 新歌入库 | 通过后台导入信息表/字段入库时，同步补充缺失信息标签入库 | 由曲库管理员手动批处理信息导入 | P1 |
|  |  | 通过填入指定新歌基础信息或网络原文件地址后，自动提取补充缺失信息或文件 | 由曲库管理员手动处理确认最终信息后导入 | P3 |
| 资源校验 | 文件验证 | 通过比对对文件身份码以及抽取画面帧校验资源文件完整性 | 由曲库管理员自动批处理 | P2 |
| 资源预览 | 预览文件 | 通过在线查看各类曲目媒体或文本资源文件检查正确性 | 由曲库管理员手动处理 | P1 |
| 预缓存同步 | 入库预缓存 | 通过调用各个CDN平台相关服务将新内容同步到CDN | 由曲库管理员入库校验后手动处理 | P2 |
| 缓存更新 | 变更更新缓存 | 在修改了媒体文件或字段属性后，通过单点或批处理更新其各CDN缓存内容 | 由曲库管理员提交更新后手动处理 | P1 |
| 筛选查询 | 基础字段筛查 | 通过对名称/编号/标签/状态/时间等基础字段任意组合筛查 | 由曲库管理员手动处理 | P1 |
|  | 关联信息子字段筛查 | 通过对关联类信息的子级字段任意组合筛查 | 由曲库管理员手动处理 | P2 |
|  | 异常资源筛查 | 通过无文件/低访问/字段不全任意组合筛查 | 由曲库管理员手动处理 | P2 |
|  | 歌曲信息筛查 | 通过对歌曲信息字段/高访问任意组合筛查 | 由曲库管理员手动处理 | P1 |
|  | 歌手信息筛查 | 通过对歌手信息字段/高访问任意组合筛查 | 由曲库管理员手动处理 | P1 |
|  | 专辑信息筛查 | 通过对专辑信息字段/高访问任意组合筛查 | 由曲库管理员手动处理 | P2 |
|  | 歌单信息筛查 | 通过对歌单信息字段/高访问任意组合筛查 | 由曲库管理员手动处理 | P2 |
|  | 栏目信息筛查 | 通过对栏目信息字段/高访问任意组合筛查 | 由曲库管理员手动处理 | P1 |
| 报表导出 | 手动导出报表 | 通过对查询结果批量选择导出指定报表 | 由曲库管理员手动处理 | P2 |
|  | 定时自动报表 | 通过设置时间点导出指定查询结果类报表 | 由曲库管理员配置 | P2 |
|  | 定制字段报表 | 通过配置字段名称自定义报表 | 由曲库管理员配置 | P3 |
|  | 定时订阅报表人员 | 对置时间点并指定查询结果类报表配置接收人员邮件 | 由曲库管理员配置 | P2 |
|  | 报表历史记录 | 记录所有报表生成记录时间和操作员 | 由曲库管理员手动处理 | P1 |
| 元数据编辑 | 字段更新 | 对条目元数据基础字段选择性修改 | 由曲库管理员手动处理 | P1 |
|  | 字段更新历史 | 记录所有更新记录时间和操作员 | 由曲库管理员手动处理 | P1 |
| 元数据编辑 | 关联更新 | 对条目元数据关联类字段选择性修改 | 由曲库管理员手动处理 | P1 |
|  | 关联更新历史 | 记录所有更新记录时间和操作员 | 由曲库管理员手动处理 | P1 |
| 下架处理 | 歌曲下架 | 选择指定或批处理直接下架歌曲 | 由曲库管理员手动处理 | P1 |
|  | 歌手下架 | 选择指定或批处理直接下架歌手，可选择其关联的所有歌曲均下架 | 由曲库管理员手动处理 | P1 |
|  | 专辑下架 | 选择指定或批处理直接下架专辑，可选择其关联的所有歌曲均下架 | 由曲库管理员手动处理 | P1 |
|  | 歌单下架 | 选择指定或批处理直接下架歌单，可选择其关联的所有歌曲均下架 | 由曲库管理员手动处理 | P1 |
|  | 栏目下架 | 选择指定或批处理直接下架栏目，可选择其关联的子项内容均下架 | 由曲库管理员手动处理 | P1 |
|  | 版权类下架 | 选择指定或批处理直接下架歌曲，并同时标记版权类信息和描述原因 | 由曲库管理员手动处理 | P1 |
|  | 版权类下架记录 | 记录所有版权下架记录时间和操作员 | 由曲库管理员手动处理 | P1 |



