---
layout: post
title: 代码坏味对应的重构方法
author: suxinde2009
category: DeginPatterns
date: 2018-04-21
---


## 1. 重复代码 （Deplicated Code）

- 形成 Template Method
- 用Factory Method引入多态创建
- 链构造函数
- 用Composite替换一／多之分
- 提取Composite
- 通过Adapter统一接口
- 引入Null Object

## 2. 过长函数（Long Method）

- 组合方法
- 将聚集操作搬移到Collecting Parmater
- 用Command替代条件调度程序
- 将聚集操作搬移到Visitor
- 用Strategy替换条件逻辑

## 3. 条件逻辑太复杂（Conditional Complexity）

- 用Strategy替换条件逻辑
- 将装饰功能搬移到Decorator
- 用State替换状态改变条件语句
- 引入Null Object


## 4. 基本类型偏执 （Primitive Obsession）

- 用类替换类型代码
- 用State替换状态改变条件语句
- 用Strategy替换条件逻辑
- 用Composite替换隐含树
- 用Interpreter替换隐式语言
- 将装饰功能搬移到Decorator
- 用Builder封装Composite


## 5. 不恰当的暴露 （Indecent Exposure）

- 用Factory封装类

## 6. 解决方法蔓延 （Solution Sprawl）

- 将创建知识搬移到Factory

## 7. 异曲同工的类 （Alternative Classes with Different Interfaces）

- 通过Adapter统一接口

## 8. 冗赘类 （Lazzy Class）

- 内联Singleton

## 9. 过大的类（Large Class）

- 用Command替换条件调度语句
- 用State替换状态改变条件语句
- 用Interpreter替换隐式语言

## 10. 分支语句 （Switch Statement）

- 用Command替换条件调度语句
- 将聚集操作搬移到Visitor

## 11. 组合爆炸 （Combinatorial Explosion）

- 用Interpreter替换隐式语言

## 12. 怪异解决方案 （Oddball Solution）

- 通过Adapter统一接口
