---
layout: post
title: spring对WebSocket支持
date: 2015-04-26 23:11
categories: [Spring]
tags: []
---
WebSocket实现了浏览器和服务器之间的双向通讯。
在浏览器中通过http仅能实现单向的通信,
comet可以一定程度上模拟双向通信,但效率较低,并需要服务器有较好的支持;
flash中的socket和xmlsocket可以实现真正的双向通信
现在很多网站做通讯使用轮询技术，但是轮询需要浏览器间隔时间向服务器发请求，带来的影响就是：浏览器需要不停地向服务器发出请求，还有就是发出的请求头很大。性能降低。

浏览器和服务器只需要要做一个握手的动作，然后，浏览器和服务器之间就形成了一条快速通道。两者之间就直接可以数据互相传送。在此WebSocket 协议中，为我们实现即时服务带来了两大好处：1. Header 互相沟通的Header是很小的-大概只有 2 Bytes 2. Server Push
Spring 4.0的一个最大更新是增加了websocket的支持。websocket提供了一个在web应用中的高效、双向的通讯，需要考虑到客户端（浏览器）和服务器之间的高频和低延时消息交换。一般的应用场景有：在线交易、游戏、协作、数据可视化等。
