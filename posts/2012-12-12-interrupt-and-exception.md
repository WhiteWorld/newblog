date: 2012-12-12
layout: post
title: "中断和异常"
description: ""
category: "学习"
tags: [Linux, 中断, 异常, 笔记]

**中断**：异步中断，由外部设备依照CPU时钟信号随机产生。由定时器和I/O设备产生的。
- 可屏蔽中断
- 非屏蔽中断

**异常**：又叫同步中断，是当前指令执行时由CPU控制单元产生的，一条指令执行完成之后CPU才会发出中断。异常是由程序的错误产生的（发送信号处理异常），或者是内核必须处理的异常条件产生的（如缺页、int指令等）。

