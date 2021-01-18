---
layout: post
title: "The Future of Frontend Technology Development in My Eyes"
---

## 一、React 没有未来  
*1. React Has No Future*  

**React 解决了什么问题？**  
*What problem does React solve?*  

- **组件化的问题**  
  *The componentization problem*
  
- **引入了虚拟 DOM 优化渲染**  
  *Introducing Virtual DOM to optimize rendering*

组件化的问题，Web Component 已经在路上了，终将有一个标准化的实现。  
*The componentization issue is already being addressed by Web Components, which will eventually lead to a standardized solution.*  

我们知道，VirtualDOM 可以一定程度上优化 DOM 渲染性能，但是在浏览器层面上 DOM 渲染性能本身就已经在优化了，React 中使用 VirtualDOM 来优化性能问题，这个问题很大程度上是 React 自己造成的。  
*We know that the Virtual DOM can optimize DOM rendering to some extent, but browser-level DOM rendering performance has already been improving. The performance problems React tries to solve with Virtual DOM are, in many ways, caused by React itself.*  

浏览器本身 DOM 性能已经很高了。当然我们也要知道 React VirtualDOM 不只是为了解决渲染问题，也为了能够实现渲染层抽象，适配更多的渲染引擎。  
*The browser's native DOM performance is already quite high. Moreover, it’s important to note that React's Virtual DOM isn’t just about solving rendering problems but also abstracts the rendering layer to support multiple rendering engines.*

## 二、Webpack 没有未来  
*2. Webpack Has No Future*  

我们之所以使用 Webpack 来打包主要是解决两个问题：  
*We use Webpack primarily to solve two problems:*  

- **模块化**  
  *Modularization*  

- **合并文件以降低创建网络链接对页面加载性能的影响**  
  *Combining files to reduce the performance impact of creating multiple network connections*  

随着 HTTP/2/3/QUIC 的发展，连接复用技术已经可以实现，即使在页面上写多个相同域的多个 script 标签也只会创建一个 TCP 链接，而且支持交叉数据传递，对网络加载性能影响很小。  
*With the development of HTTP/2, HTTP/3, and QUIC, connection multiplexing has become possible. Even if multiple script tags from the same domain are used on a page, only one TCP connection is created, and it supports cross-data transmission, minimizing the impact on network performance.*  

目前很多 CDN 厂商都已经部署了 HTTP/2（\w QUIC）协议，毕竟对他们来说也是一个节省开销的好事情。  
*Many CDN providers have already deployed HTTP/2 (and QUIC) protocols, as it is also cost-efficient for them.*  

其次，浏览器对于 ES Module 已经支持的很好了，而且从社区支持来看越来越多的 Library 都输出了符合 ESM 规范的打包格式。而且 ESM 相比于其他打包格式还有一些诸如减少 JS VM 虚拟机计算量等额外优势，没有理由不支持。  
*In addition, browsers now have excellent support for ES Modules, and more libraries are providing bundles in ESM format. Compared to other formats, ESM also reduces the JS VM's workload, which offers compelling advantages.*  

**没有了 Webpack，TypeScript 怎么办？**  
*What About TypeScript Without Webpack?*  

如果没有了 Webpack，那么 TypeScript 可以通过 WebAssembly 在浏览器端解析和执行，无需预编译执行。  
*Without Webpack, TypeScript could be parsed and executed via WebAssembly directly in the browser, eliminating the need for precompilation.*

## 三、小程序没有未来  
*3. Mini Programs Have No Future*  

虽然目前小程序已经很流行，但是 Service Worker 和 Offline App 的广泛应用是迟早的事情。  
*Although mini programs are quite popular right now, the widespread adoption of Service Workers and offline apps is inevitable.*  

小程序总是想着向 Native 的方向努力，最终很可能会变成 Native 开发的一种方式，而非 Web 的未来。  
*Mini programs tend to evolve toward native app development, which will likely make them another form of native development, rather than the future of the web.*  

虽然小程序为开发者提供了一种简单、快速的开发方式，但它并没有实现重大创新。  
*While mini programs provide a simple and fast development approach, they haven't brought any groundbreaking innovations.*

## 我眼中的未来是什么？  
*What Do I See as the Future?*  

**回归标准：**  
*Returning to Standards:*  
我在讲某个东西没有未来并不是说否定它存在的意义，在特定的时期下它们的存在是非常重要的，它们加速了 Web 发展进程功不可没，但是缺乏标准化总是在解决一个问题的同时带来了非常多衍生的其他问题，这就是**工程化实践**和**标准化实践**的区别。  
*When I say that something has no future, it doesn’t negate its significance. At certain stages, these technologies have been vital to accelerating the web’s development. However, the lack of standardization often leads to many secondary issues while solving a core problem. This is the difference between **engineering practices** and **standardized practices**.*  

**大道至简：**  
*Simplicity Is the Ultimate Sophistication:*  
想想看，我们现在要开始做一个 Web 应用要做那些事情？安装一大堆的框架、工具库、工具链、打包编译工具，每修改一个文件都要等待漫长的编译，每次发布都要经过复杂的工作流程来确保与开发时的预期一致。我认为未来不是这样，就应该是开箱即用，唾手可得，且性能优异。  
*Think about it—what do we need to do to start a web application today? Install countless frameworks, libraries, toolchains, and bundlers. Every file modification requires lengthy recompilation, and each release goes through complex workflows to ensure consistency with development expectations. I believe the future won’t be like this. It should be plug-and-play, readily available, and highly performant.*  