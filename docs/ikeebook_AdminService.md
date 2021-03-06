---
Title: ikeeBook 后台管理系统
---

# ikeeBook 管理后台系统
- PM：赵正奇
- 作者：走走

## Overview
后台管理系统是ikeebook管理人员，对后台数据（用户，明信片，文章）进行，`查看`，`单/多个数据对象操作`，`信息统计`等多项操作。

## Context
需要后台管理的功能有以下几点：
- 用户账户管理： 对普通用户账户进行操作，对特殊用户的操作（问题用户，合作用户等），对用户的Footprint的查看和信息汇总。
- 内容管理：对普通文章/明信片的操作（推荐，关注），对特殊文章/明信片的操作（黑名单，删除，沙盒等。）
- 安全：安全的登陆方式，安全审核。

## Scope
### Required
* 基于当前的后端系统架构（Spring+MyBatis）添加后台系统管理功能，无需独立构建独立的后端系统。
* 设计/建造 对应功能Restful APIs，给前端使用。
* 修改 当前的数据库 以满足后台管理系统的的业务需求。

### Good to have
* 建立基本的测试环境

### Out of Scope
* 独立的后端系统架构及部署。

## Current System
DragonService 是一个以springBoot+Mybatis为架构，以MySQL和Redis为数据工具的，面向普通用户注册登陆和内容管理查看的内容管理平台。其已经实现了多个对于用户，内容，功能等操作的API。并`预留了管理用户的入口`，以及管理员用户的数据表及数据结构。

![Diagram](http://yuejoo.github.io/SharedDocuments/CurrentSystem.svg)