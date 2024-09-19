---
layout: post
title: "Container Strategies and Concerns of Internet Titans"
---

随着科技的迅猛发展，我们日常使用的手机应用不再是单一的本地软件，而是逐渐向着更为复杂和多元化的形态演变。如今，许多应用都采用了 **Hybrid App** 的架构，即通过结合 **Native** 的基础功能与 **Webview + JS Bridge** 来实现快速迭代和内容更新。在这一模式中，**Webview** 的渲染性能成为了用户体验的关键，因为它直接影响着界面的响应速度、流畅度以及视觉效果。  

*As technology advances rapidly, the apps we use on a daily basis have evolved from simple local software to more complex and diversified forms. Many applications now adopt the architecture of **Hybrid App**, combining **Native** functionalities with **Webview + JS Bridge** to achieve quick iteration and content updates. In this model, the rendering performance of **Webview** is crucial, as it directly affects the responsiveness, smoothness, and visual quality of the interface.*

### 巨头的布局：浏览器内核的重要性  

*Strategic Moves of Tech Giants: The Importance of Browser Kernels*

看到这一趋势，互联网巨头们纷纷加大了对浏览器内核的研发与收购力度。浏览器内核不仅仅是一个工具，更是企业提升用户体验、增强技术控制力的战略性资产。  

*In response to this trend, internet giants are ramping up efforts to develop and acquire browser kernels. A browser kernel is not just a tool; it's a strategic asset that enhances user experience and strengthens technical control for these companies.*

例如，**阿里巴巴** 通过收购 **UC 浏览器**，获得了其自有的浏览器内核，并将其应用于多款阿里系产品中；**腾讯** 拥有自主研发的 **X5 内核**，并通过收购 **搜狗浏览器** 进一步增强了自身的浏览器技术储备。**字节跳动** 也不甘示弱，基于 **WebKit** 技术积极开发自己的浏览器内核，以应对旗下产品日益复杂的前端需求。  

*For example, **Alibaba** acquired **UC Browser**, gaining its proprietary browser kernel, which is now used across multiple Alibaba products. **Tencent** has its self-developed **X5 kernel**, and further strengthened its browser tech through the acquisition of **Sogou Browser**. **ByteDance** is also catching up, actively developing its own browser kernel based on **WebKit** to handle the increasing complexity of front-end needs across its products.*

相比之下，**美团** 虽然在小程序架构上做出了巨大的商业推动，但由于没有自研的浏览器内核，它在技术战略上面临了一定的制约。为此，美团启动了自己的浏览器内核研发计划，并尝试 **fork WebKit** 来建立自有的内核。然而，由于 WebKit 庞大且复杂的代码库，这一计划的推进并不顺利。  

*In contrast, **Meituan**, while pushing forward its mini-program architecture from a business standpoint, has been technically constrained by its lack of an in-house browser kernel. To address this, Meituan started its own browser kernel development plan, attempting to **fork WebKit** to create its kernel. However, the complexity and size of the WebKit codebase have hindered progress.*

### 渲染技术的变革：从 React Native 到 Flutter  

*The Shift in Rendering Technologies: From React Native to Flutter*

在 WebKit 内核开发受阻的背景下，当 **React Native** 技术崭露头角时，美团看到了新的希望。React Native 提供了基于 JavaScript 的跨平台解决方案，允许开发者通过一套代码实现 iOS 和 Android 两端的渲染。然而，React Native 的局限性也逐渐显现，尤其是其性能问题和复杂的原生模块绑定模式，令其难以真正实现“多端一致性”。  

*With the stagnation of WebKit kernel development, the emergence of **React Native** brought new hope for Meituan. React Native offers a cross-platform solution based on JavaScript, allowing developers to use one codebase to render on both iOS and Android. However, the limitations of React Native became apparent, particularly its performance issues and the complexity of native module bindings, making it difficult to achieve true "multi-end consistency".*

这时，**Flutter** 的出现为行业提供了全新的解决思路。不同于 React Native，Flutter 从底层重新构建了自己的渲染引擎，完全绕过了操作系统的 UI 组件，直接使用 **Skia（基于 OpenGL）** 来进行图形渲染。这一架构设计使得 Flutter 在跨平台性能上具备了显著优势。  

*At this point, the arrival of **Flutter** provided a new solution for the industry. Unlike React Native, Flutter rebuilt its rendering engine from the ground up, bypassing the OS’s UI components and directly using **Skia (based on OpenGL)** for graphic rendering. This architecture gives Flutter a significant performance advantage in cross-platform scenarios.*

从我的个人经历来看，我也从最初的工程化方案研究，逐渐转向小程序架构，再进入 Flutter 渲染引擎的开发项目中。我们的目标是基于 **Skia** 解析 **DOM** 和 **CSS**，以期打造一个高效的渲染引擎。尽管这项工作还在进行中，但我们坚信 Flutter 的技术路线是值得长期投入的。  

*From my own experience, I have shifted from initial engineering solution research to mini-program architecture, and then into the development of the Flutter rendering engine. Our goal is to build an efficient rendering engine by parsing **DOM** and **CSS** using **Skia**. Although this work is ongoing, we are confident that Flutter's technological path is worth long-term investment.*

### React Native 的困境与 Flutter 的优势  

*The Struggles of React Native and the Advantages of Flutter*

尽管 React Native 在跨平台领域曾一度风靡，但其复杂的原生绑定模式始终是开发者面临的一个难题。由于其核心是基于 **Native** 组件的封装，开发者不得不频繁地进行原生代码的编写和调试，这与其最初的“跨平台一致性”愿景背道而驰。  

*Though React Native once gained popularity in the cross-platform field, its complex native binding model has always been a challenge for developers. Since it is fundamentally based on **Native** component wrapping, developers often have to write and debug native code, diverging from the original goal of "cross-platform consistency".*

相反，Flutter 通过重新构建渲染引擎，避免了操作系统层面的依赖，真正做到了“一次编写，处处运行”。从技术的角度来看，Flutter 为开发者提供了更大的灵活性和一致的用户体验。与此同时，它还解决了 React Native 无法绕过的一些固有问题，尤其是在复杂 UI 和动画渲染上的优势明显。  

*On the other hand, Flutter rebuilt its rendering engine, avoiding OS-level dependencies, truly achieving "write once, run anywhere". From a technical standpoint, Flutter offers developers greater flexibility and a consistent user experience. It also addresses some inherent issues that React Native could not overcome, particularly in complex UI and animation rendering.*

### 挑战与未来展望  

*Challenges and Future Outlook*

然而，尽管 **Flutter** 在架构上占据优势，但它并不是一个“完美的解决方案”。例如，基于 Flutter 开发的 **闲鱼** App，尽管在开发效率上有所提升，但其稳定性和性能仍然存在进一步优化的空间。这反映出，尽管 Flutter 具备巨大的潜力，但在实际的应用场景中，它依然面临诸多挑战。  

*However, despite **Flutter**'s architectural advantages, it is not a "perfect solution". For example, the **Xianyu** app, developed with Flutter, has shown improved development efficiency, but its stability and performance still require further optimization. This reflects that while Flutter has enormous potential, it still faces many challenges in real-world applications.*

总的来说，随着移动互联网的持续演进，各大互联网公司在容器技术领域的布局和战略不断调整。浏览器内核的研发、跨平台架构的选择，甚至是渲染引擎的优化，都是决定未来用户体验的关键要素。在这个技术变革与创新并存的时代，机会与挑战并存，每一个选择都将深刻影响未来的市场格局。  

*In summary, as mobile internet continues to evolve, internet companies are constantly adjusting their strategies in the field of container technology. The development of browser kernels, the choice of cross-platform architectures, and even the optimization of rendering engines are all key elements in shaping the future user experience. In this era of technological change and innovation, opportunities and challenges coexist, and every choice will profoundly impact the future market landscape.*

通过丰富的技术积累与快速响应的市场策略，互联网巨头们将在未来的容器技术赛道上继续角逐。而开发者也需要紧跟时代潮流，选择合适的技术方案，才能在这场技术革命中占据一席之地。  