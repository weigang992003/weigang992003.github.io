---
layout: post
title:  "Opennebula integration guide"
date:   2016-01-13 15:03:00
categories: tech
---

## 1.1 Overview
OpenNebula被设计为易于适应任何基础设施，易于扩展新的组件。所以它是一个模块化的系统，可以对接各种云架构系统和数据中心服务器。在本指南中我们回顾一下OpenNebula的主要接口,包括他们的使用，如何查看更详细的文档。
有2类典型的接口：终端用户云、系统接口。

### 1.1.1 如何阅读

Cloud interface 云接口用于开发面向终端用户的工具，他们提供了高度抽象的函数。用于管理虚拟机、网络、镜像，通过调用REST API。Cloud interface隐藏了复杂性以适用于终端用户。OpenNebula实现了EC2接口，可以管理Amazon的虚拟机。可以调用EC2的查询工具访问OpenNebula云。如果开发门户、工具或者其他终端用户的需求，使用cloud interface.

System interfaces包含了完整的OpenNebula功能，主要用于适应目标设施：

- XML-RPC接口是OpenNebula的主要接口，包含了OpenNebula的所有功能。通过XML-RPC可以控制、管理OpenNebula的所有资源，包括VMs,
Virtual Networks, Images, Users, Hosts 和
Clusters.使用XML-RPC接口可以开发特定的云应用类库或者与核心交互的底层接口.

- OpenNebula Cloud API提供了一种便捷的交互与OpenNebula的核心XMLRPC API。OCA接口覆盖了XML-RPC相同的功能。OCA绑定了两种语言:Ruby, Java.

- OpenNebula OneFlow
API提供了RESTful风格的服务用于创建、控制和监控虚拟机与部署依赖的关系。

### 1.1.2 虚拟机兼容性
上述接口兼容KVM, vCenter

## 1.2 XML-RPC API
所有的xml-rpc响应包含3个值，第1、3两个值是固定的，但是第2个值会包含错误信息如果有错的话。

Note: 所有的方法期待一个与连接用户相关的session
字符串作为第一个参数。字符串的格式在ONE_AUTH中定义，默认是<username>:<password>


Note: 每一个XML-RPC请求都必须进行认证和鉴权(authenticated and authorized)


