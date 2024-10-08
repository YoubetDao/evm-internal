# 创建 TODO 合约

## 关于本节

在本小节中，我们将学习如何创建一个简单的 Solidity 合约文件，并介绍合约文件的基本结构。我们将编写一个名为 `TodoList` 的合约，它最终会成为一个功能完善的任务管理合约（TODO List）。

## 合约结构概述

每个 Solidity 合约文件基本由以下几个部分组成：

1. **版本声明**：指定使用的 Solidity 编译器版本。
2. **合约定义**：定义合约的名称和功能。
3. **状态变量**：存储合约的数据(不包含在本小节)。
4. **构造函数**：初始化合约状态(不包含在本小节)。
5. **函数**：定义合约的行为逻辑(不包含在本小节)。

### 创建合约文件

在 `contracts/` 创建一个新的 Solidity 文件，命名为 `TodoList.sol`, 文件内容:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

contract TodoList {
    // TODO: 在这里定义状态变量和函数
}
```

## 文件结构说明：

**`SPDX-License-Identifier: MIT`**：这是一种许可证声明. 推荐为合约提供开源许可证（MIT），表明代码可自由使用。**根据作者的实际开发经验，每次使用的都是 MIT。**

**`pragma solidity ^0.8.24;`**：这是 Solidity 版本声明. ^ 是称为“插入符”（caret）的符号，用来指定 Solidity 编译器版本的兼容性. 该行语言是: 至少是 0.8.24，但 小于 0.9.0 的任意版本。

**如何设置合适的版本呢?** 如果你使用 hardhat , 参考 `hardhat.config.ts` 中 `solidity.compilers.version` 字段, 保持一致即可。

**`contract TodoList`**：这是合约的声明. **contract** 是一个关键字, 用来定义一个智能合约, 它类似于编程中的类（class）。`TodoList` 是合约的名称, 合约的功能将在这个结构内实现。

## 小结

这一小节我们简单介绍了 Solidity 合约文件的基础结构，并创建了一个空的合约文件。下一小节我们将开始定义 TODO 合约的状态变量。

## 附加资源

1. **Version Pragma**：阅读 Solidity 的 [官方文档](https://docs.soliditylang.org/en/v0.8.27/layout-of-source-files.html#pragma) 来深入了解版本控制的使用和目的。

2. **Solidity 版本区别**：研究 Solidity 0.8.x 系列的更新内容，了解为何选择这个版本作为合约编写的起点。参考这篇 [Solidity 0.8.x 更新说明](https://docs.soliditylang.org/en/v0.8.27/080-breaking-changes.html). 这份文档是为了帮助你了解一些基础知识，不需要花很多时间深入学习，先大概浏览一下就好。等到以后遇到问题时，可以随时回来查阅。

3. **智能合约的开源许可证**：深入了解不同的智能合约许可证（如 MIT、GPL 等），以及它们对项目的影响。可以参考 [SPDX 许可证列表](https://spdx.org/licenses/)。
