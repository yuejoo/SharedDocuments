- [UseCases](#usecases)
  * [1. Dashboard（基础板块）](#1-dashboard------)
    + [Workflow](#workflow)
    + [Data Model](#data-model)
  * [2. 文章板块](#2-----)
    + [2.1 请求文章管理信息](#21---------)
      - [Workflow](#workflow-1)
      - [DataModel （TODO）](#datamodel--todo-)
    + [2.2 修改文章信息](#22-------)
      - [2.2.1 将文章（原文）加入人工推荐](#221--------------)
        * [Workflow](#workflow-2)
      - [2.2.2 将文章（原文）加入短期推荐](#222--------------)
        * [Workflow](#workflow-3)
      - [2.2.3 将文章（原文）加入黑名单](#223-------------)
        * [Workflow](#workflow-4)
      - [2.2.4 将文章（原文）删除](#224----------)
        * [Workflow](#workflow-5)
      - [2.2.5 修改文章（原文）的备注信息](#225--------------)
        * [Workflow](#workflow-6)
      - [2.2.6 and 7 沙盒相关（TODO：明确沙盒是什么）](#226-and-7------todo---------)
        * [Workflow](#workflow-7)
  * [3. 用户信息板块](#3-------)
    + [3.1 请求用户管理信息](#31---------)
      - [Workflow](#workflow-8)
      - [DataModel （TODO）](#datamodel--todo--1)
    + [3.2 给用户添加分组](#32--------)
      - [Workflow](#workflow-9)
    + [3.3 将用户加入禁言名单](#33----------)
      - [Workflow](#workflow-10)
    + [3.4 一系列显示功能（TODO: need more details.）](#34---------todo--need-more-details-)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

# TODO
## Missing Data
### 文章
* 文章类型（or 推荐类型） （推荐， 短期推荐，文章沙盒， 敏感沙盒，黑名单）（5 类）
* 管理员备注

### 用户
* 用户类型 （合作用户，认证作者，认证译者，重点用户，观察用户，黑名单用户，敏感用户）（7 类）

# UseCases
## 1. Dashboard（基础板块）
Dashboard是用户管理界面的基本信息统计显示页面。显示必要而简单的信息统计。
### Workflow
* *管理用户*请求当前的Dashboard
* *管理系统*计算当前Dashboard信息
* *管理系统*反回统计信息或错误码。

### Data Model
* 多个规定时间段内的 文章统计
* 多个规定时间段内的 文章语言类别统计
* 多个规定时间段内的 用户语言占比统计

## 2. 文章板块
### 2.1 请求文章管理信息
#### Workflow
* *管理用户*请求**N条**文章信息基于**某时间段**（例如当天，昨天等）内的搜索。
* *管理系统*统计并合成文章信息
* *管理系统*返回文章信息或错误码。
* *管理用户*请求**下一页N条**文章信息基于**某时间段**（例如当天，昨天等）内的搜索。
* *管理系统*统计并合成文章信息
* *管理系统*返回文章信息或错误码。
* *管理用户*请求**N条**文章信息基于**其他时间段**（例如当天，昨天等）内的搜索。
* *管理系统*统计并合成文章信息
* *管理系统*返回文章信息或错误码。

#### DataModel （TODO）
TODO：add detailed data model

### 2.2 修改文章信息
#### 2.2.1 将文章（原文）加入人工推荐
##### Workflow
* *管理用户*请求将单个或多个文章id加入推荐列表。
* *管理系统*将修改对应内容
* *管理系统*通知文章作者相应操作。
* *管理系统*反回成功或错误码。

#### 2.2.2 将文章（原文）加入短期推荐
##### Workflow
* *管理用户*请求将单个或多个文章id加入推荐列表。
* *管理系统*将修改对应内容
* *管理系统*通知文章作者相应操作。
* *管理系统*反回成功或错误码。

#### 2.2.3 将文章（原文）加入黑名单
##### Workflow
* *管理用户*请求将单个或多个文章id加入黑名单。
* *管理系统*将修改对应内容
* *管理系统*通知文章作者相应操作。
* *管理系统*反回成功或错误码。

#### 2.2.4 将文章（原文）删除
##### Workflow
* *管理用户*请求将单个或多个文章id删除。
* *管理系统*将修改对应内容（同时删除所有译文）
* *管理系统*通知文章作者相应操作。
* *管理系统*反回成功或错误码。

#### 2.2.5 修改文章（原文）的备注信息
##### Workflow
* *管理用户*请求添加或修改文章的备注信息。
* *管理系统*将修改对应内容
* *管理系统*反回成功或错误码。

#### 2.2.6 and 7 沙盒相关（TODO：明确沙盒是什么）
##### Workflow
* *管理用户*请求将文章添加进沙盒
* *管理系统*将修改对应内容
* *管理系统*反回成功或错误码。

## 3. 用户信息板块
### 3.1 请求用户管理信息
#### Workflow
* *管理用户*请求**N条**用户信息基于**某时间段**（例如当天，昨天等）内的搜索。
* *管理系统*统计并合成用户信息
* *管理系统*返回用户信息或错误码。
* *管理用户*请求**下一页N条**文用户信息基于**某时间段**（例如当天，昨天等）内的搜索。
* *管理系统*统计并合成用户信息
* *管理系统*返回用户信息或错误码。
* *管理用户*请求**N条**用户信息基于**其他时间段**（例如当天，昨天等）内的搜索。
* *管理系统*统计并合成用户信息
* *管理系统*返回用户信息或错误码。

#### DataModel （TODO）
TODO：add detailed data model

### 3.2 给用户添加分组
#### Workflow
* *管理用户*请求将单个或多个用户加入某特定分组
* *管理系统*将用户加入该分组
* *管理系统*返回成功信息或错误码。

### 3.3 将用户加入禁言名单
#### Workflow
* *管理用户*请求将单个或多个用户在某个时间段加入禁言名单
* *管理系统*将用户加入该分组
* *管理系统*返回成功信息或错误码。

### 3.4 一系列显示功能（TODO: need more details.）