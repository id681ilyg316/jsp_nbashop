## 本项目实现的最终作用是基于JSP实现NBA及其周边用品销售平台
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 会员管理
 - 友情链接管理
 - 商品库存管理
 - 商品管理
 - 商品类别管理
 - 滚动图片管理
 - 球队管理
 - 留言管理
 - 管理关于我们
 - 管理员登录
 - 订单管理
 - 资讯管理
### 第2个角色为用户角色，实现了如下功能：
 - 修改个人信息
 - 提交留言
 - 提交订单
 - 查看商品详情
 - 查看我的订单
 - 查看购物车
 - 查看首页
 - 用户登录
 - 确认支付
## 数据库设计如下：
# 数据库设计文档

**数据库名：** nbashop

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [about](#about) | 关于我们信息表 |
| [addr](#addr) |  |
| [car](#car) |  |
| [chat](#chat) |  |
| [dddetail](#dddetail) |  |
| [ddinfo](#ddinfo) |  |
| [fav](#fav) | 商品收藏表 |
| [goods](#goods) |  |
| [imgadv](#imgadv) |  |
| [kcrecord](#kcrecord) |  |
| [lookrecord](#lookrecord) |  |
| [member](#member) | 会员表 |
| [news](#news) | 新闻资讯表 |
| [pj](#pj) |  |
| [ppinfo](#ppinfo) |  |
| [protype](#protype) |  |
| [scan_his](#scan_his) |  |
| [siteinfo](#siteinfo) |  |
| [sysuser](#sysuser) |  |
| [yqlink](#yqlink) |  |

**表名：** <a id="about">about</a>

**说明：** 关于我们信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | lxr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 联系人  |
|  3   | tel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  4   | addr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 地址  |
|  5   | note |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="addr">addr</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | shr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | shrtel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | shraddr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | memberid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 会员ID  |
|  6   | delstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 删除状态  |

**表名：** <a id="car">car</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | gid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | mid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | sl |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="chat">chat</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | msg |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  3   | hfmsg |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  4   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |
|  5   | memberid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 会员ID  |

**表名：** <a id="dddetail">dddetail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | ddno |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 订单号  |
|  3   | goodid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | sl |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="ddinfo">ddinfo</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | ddno |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 订单号  |
|  3   | memberid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 会员ID  |
|  4   | ddprice |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | fhstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  6   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |
|  7   | shstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 审核状态  |
|  8   | wlinfo |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  9   | fkstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 付款状态  |
|  10   | shrname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  11   | shrtel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  12   | shraddr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="fav">fav</a>

**说明：** 商品收藏表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | goodid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | memberid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 会员ID  |

**表名：** <a id="goods">goods</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | goodno |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | goodname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | fid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | sid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  6   | price |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 价格  |
|  7   | note |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  8   | saver |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 上传者  |
|  9   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |
|  10   | shstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 审核状态  |
|  11   | istj |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否特价  |
|  12   | tprice |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 特价价格  |
|  13   | filename |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 文件名  |
|  14   | delstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 删除状态  |
|  15   | salestatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  16   | goodpp |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="imgadv">imgadv</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | filename |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 文件名  |

**表名：** <a id="kcrecord">kcrecord</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | gid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | happennum |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | TYPE |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 类型  |
|  5   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |

**表名：** <a id="lookrecord">lookrecord</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | memberid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 会员ID  |
|  3   | goodid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |

**表名：** <a id="member">member</a>

**说明：** 会员表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | uname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  3   | upass |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  4   | email |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 邮箱  |
|  5   | tname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 真实名字  |
|  6   | sex |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 性别  |
|  7   | addr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 地址  |
|  8   | ybcode |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  9   | QQ |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | QQ号码  |
|  10   | tel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  11   | delstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 删除状态  |
|  12   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |

**表名：** <a id="news">news</a>

**说明：** 新闻资讯表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 标题  |
|  3   | note |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  4   | img |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 照片  |
|  5   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |
|  6   | TYPE |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 类型  |

**表名：** <a id="pj">pj</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | goodid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | goodsaver |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | memberid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 会员ID  |
|  5   | jb |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  6   | msg |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  7   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |
|  8   | hf |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="ppinfo">ppinfo</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | ppname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | delstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 删除状态  |

**表名：** <a id="protype">protype</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | typename |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 类型名称  |
|  3   | fatherid |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 父分类ID  |
|  4   | delstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 删除状态  |

**表名：** <a id="scan_his">scan_his</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | scan_his_key |   varchar   | 2000 |   0    |    Y     |  N   |   NULL    |   |
|  2   | value |   varchar   | 2000 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="siteinfo">siteinfo</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | logoimg |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | sitenamefont |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | sitenameback |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | tel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  6   | addr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 地址  |
|  7   | note |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="sysuser">sysuser</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | usertype |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户类型  |
|  3   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  4   | userpwd |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  5   | realname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 真实名字  |
|  6   | sex |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 性别  |
|  7   | idcard |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 身份证信息  |
|  8   | tel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  9   | email |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 邮箱  |
|  10   | addr |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 地址  |
|  11   | delstatus |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 删除状态  |
|  12   | savetime |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 保存时间  |

**表名：** <a id="yqlink">yqlink</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   bigint   | 20 |   0    |    N     |  Y   |       |   |
|  2   | linkname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | linkurl |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**运行不出来可以微信 javape 我的公众号：源码码头**
