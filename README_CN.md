<img src="https://26805113.s21i.faiusr.com/4/ABUIABAEGAAgtrqthQYozNCRwwMwuBc43gU.png" alt="mo banner">

<div class="column" align="middle">
  <a href="https://github.com/matrixorigin/matrixone/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-Apache%202.0-red.svg" alt="license"/>
  </a>
  <a href="https://golang.org/">
    <img src="https://img.shields.io/badge/Language-Go-blue.svg" alt="language"/>
  </a>
  <img src="https://img.shields.io/badge/platform-MacOS-white.svg" alt="macos"/>
  <img src="https://img.shields.io/badge/platform-Linux-9cf.svg" alt="linux"/>
  <a href="https://www.codefactor.io/repository/github/matrixorigin/matrixone">
    <img src="https://www.codefactor.io/repository/github/matrixorigin/matrixone/badge?s=7280f4312fca2f2e6938fb8de5b726c5252541f0" alt="codefactor"/>
  </a>
  <a href="https://docs.matrixorigin.io/0.3.0/MatrixOne/Release-Notes/v0.3.0/">
   <img src="https://img.shields.io/badge/Release-v0.3.0-green.svg" alt="release"/>
  </a>
  <br>
  <a href="https://docs.matrixorigin.io/0.3.0/">
    <b>Docs</b>
  </a>
  <b>||</b>
  <a href="https://www.matrixorigin.io/">
   <b> Official Website</b>
  </a>
  <br>
  <a href="https://github.com/matrixorigin/matrixone/blob/main/README.md">
    <b>English</b>
  </a>
  <b>||</b>
  <a href="https://github.com/matrixorigin/matrixone/blob/main/README.zh.md">
    <b>简体中文</b>
  </a>
</div>

目录
========

* [MatrixOne是什么？](#what-is-matrixone)
* [核心特性](#key-features)
* [用户价值](#user-values)
* [架构](#architecture)
* [快速上手](#quick-start)
* [参与贡献](#contributing)
* [License](#license)

## MatrixOne是什么？

MatrixOne是一款面向未来的超融合异构云原生数据库，通过超融合数据引擎支持事务/分析/流处理等混合工作负载，通过异构云原生架构支持跨机房协同/多地协同/云边协同。简化开发运维，消简数据碎片，打破数据的系统、位置和创新边界。


##  🎯 <a id="key-features">核心特性</a> 
### 💥 **超融合引擎**
* **超融合引擎**
  
     融合数据引擎，单数据库即可支持TP、AP、时序、机器学习等混合工作负载。

* **内置流引擎**
  
     利用独有的增量物化视图能力，无需跨数据库即可实现实时数据流处理。

### ☁️ **异构云原生**
* **异构统一**
     
     支持跨机房协同/多地协同/云边协同，实现无感知扩缩容，提供高效统一的数据管理。

* **多地多活**
  
     MatrixOne采用最优的一致性协议，实现业内最短网络延迟的多地多活。


### 🚀 **极致的性能**

* **高性能**

     特有的因子化计算和向量化执行引擎，支持极速的复杂查询。单表、星型和雪花查询都具备极速分析性能。


* **强一致**
  
     提供跨存储引擎的高性能全局分布式事务能力，在保证极速分析性能的同时支持更新、删除和实时点查询。

* **高可用**
  
     存算分离，支持存储节点与计算节点独立扩缩容，高效应对负载变化。


## 💎 **<a id="user-values">用户价值</a>**
<details>
  <summary><b><font size=4>简化数据开发和运维</b></font></summary> 
      随着业务发展，企业使用的数据引擎和中间件越来越多，而每一个数据引擎平均依赖5+个基础组件，存储3+个数据副本，每一个数据引擎都要各自安装、监控、补丁和升级。这些都导致数据引擎的选型、开发及运维成本高昂且不可控。在MatrixOne的一体化架构下，用户使用单个数据库即可服务多种数据应用，引入的数据组件和技术栈减少80%，大大简化了数据库管理和维护的成本。
</details>
<details>
  <summary><b><font size=4>消减数据碎片和不一致</b></font></summary>
    在既有复杂的系统架构内，存在多条数据管道多份数据存储冗余。数据依赖复杂，导致数据更新维护复杂，上下游数据不一致问题频发，人工校对难度增大。MatrixOne的高内聚架构和独有的增量物化视图能力，使得下游可以支持上游数据的实时更新，摆脱冗余的ETL流程，实现端到端实时数据处理。
</details>
<details>
  <summary><b><font size=4>无需绑定基础设施</b></font></summary>
    因为基础设施的碎片化，企业的私有化数据集群和公有云数据集群之间数据架构和建设方案割裂，数据迁移成本高。而数据上云一旦选型确定数据库厂商，后续的集群扩容、其他组件采购等都将被既有厂商绑定。MatrixOne提供统一的云边基础架构和高效统一的数据管理，企业数据架构不再被基础设施绑定，实现单数据集群跨云无感知扩缩容，提升性价比。
</details>
<details>
  <summary><b><font size=4>极速的分析性能</b></font></summary>  
    目前，由于缓慢的复杂查询性能以及冗余的中间表，数据仓库在业务敏捷性上的表现不尽人意，大量宽表的创建也严重影响迭代速度。MatrixOne通过特有的因子化计算和向量化执行引擎，支持极速的复杂查询，单表、星型和雪花查询都具备极速分析性能。
</details>
<details>
  <summary><b><font size=4>像TP一样可靠的AP体验</b></font></summary>   
    传统数据仓库数据更新代价非常高，很难做到数据更新即可见。在营销风控，无人驾驶，智能工厂等实时计算要求高的场景或者上游数据变化快的场景中，当前的大数据分析系统无法支持增量更新，往往需要做全量的更新，耗时耗力。MatrixOne通过提供跨存储引擎的高性能全局分布式事务能力，支持条级别的实时增量更新，在保证极速分析性能的同时支持更新、删除和实时点查询。
</details>
<details>
  <summary><b><font size=4>不停服自动扩缩容</b></font></summary>   
    传统数仓无法兼顾性能和灵活度，性价比无法做到最优。MatrixOne基于存算分离的技术架构，支持存储节点与计算节点独立扩缩容，高效应对负载变化。
</details>

<br

## 🔎 <a id="architecture">架构一览</a>
MatrixOne作为一个从零开始打造的全新数据库，其整体架构由多个模块组成。对应架构图如下图所示：   
<p align="center">
  <img alt="MatrixOne" height="500" width="700" src="https://github.com/matrixorigin/artwork/blob/main/docs/overview/overall-architecture.png?raw=true">
</p>
<details>
  <summary><font size=4 style=IT><b>查询解析层(Query Parser Layer)</b></font></summary>

* **解析器(Parser):** 将SQL、流处理或Python语言解析为抽象语法树，以便进一步处理。

* **计划器(Planner):** 通过一系列基于规则、基于成本的优化算法找到最佳的执行计划，并将抽象语法树转换为计划树。

* **IR生成器(IR Generator):** 将Python代码转变为LLVM IR的中间码。
</details>  

<details>
  <summary><font size=4 style=IT><b>计算层</b></font></summary>

* **即时编译(JIT Compilation):** 在运行时使用LLVM将SQL计划树或IR代码转换为本地程序。

* **向量化执行(Vectorized Execution):** MatrixOne利用SIMD指令构造向量化执行通道。

* **缓存(Cache):** 用于查询的数据、索引和元数据的多版本的缓存。  

</details>
  
<details>
  <summary><font size=4 style=IT><b>集群管理层</b></font></summary>

MatrixCube是构建分布式系统的基础库，它保证数据库集群的高可靠性、强一致性和可扩展性。它用于保证分布式、有状态的应用程序构建，使开发人员只需要关注单节点的业务逻辑实现即可。MatrixCube目前基于`multi-raft`搭建来提供强一致能力，之后将迁移到`Paxos`，用于更好服务跨数据中心的应用场景。  

* **调度器(Prophet):** MatrixCube中用于管理、调度MatrixOne集群的工具。
* **事务管理器(Transaction Manager):** MatrixOne支持快照隔离级别(snapshot isolation)的分布式事务。
* **复制状态机(Replicated State Machine):** MatrixOne使用基于`raft`的共识协议和超逻辑时钟来实现集群的强一致性。


关于**MatrixCube**的更多信息，请参见[MatrixCube架构设计详解](https://docs.matrixorigin.io/cn/0.3.0/MatrixOne/Overview/matrixcube/matrixcube-introduction/)
</details>

<details>
  <summary><font size=4 style=IT><b>存储引擎层(Replicated Storage Layer)</b></font></summary>

* **行存(Row Storage):** 存储交易类负载数据、元数据和Catalog。
* **列存(Column Storage):** 存储分析负载类数据与物化视图。
</details>

<details>
  <summary><font size=4 style=IT><b>存储介质层(Storage Provision Layer)</b></font></summary>

  MatrixOne作为无需绑定底层基础设施的数据库，可以支持共享存储S3/HDFS，或本地磁盘、私有数据中心、混合云，甚至智能设备等存储介质的数据存储。

</details>
<br>

**[MatrixOne技术设计](https://docs.matrixorigin.io/0.3.0/MatrixOne/Overview/MatrixOne-Tech-Design/matrixone-techdesign/)** 将对你理解MatrixOne架构有一定帮助。  

## ⚡️ <a id="quick-start">快速上手</a>
按照以下步骤快速开始使用MatrixOne。
### ⚙️ 安装MatrixOne
MatrixOne supports Linux and MacOS. You can install MatrixOne either by [building from source](#building-from-source) or [using docker](#using-docker).
#### 使用源代码搭建

**1.** 搭建Go语言环境（至少需要1.17版本）。
  
**2.** 获取MatrixOne源码

```
$ git clone https://github.com/matrixorigin/matrixone.git
$ cd matrixone
```

**3.** 运行编译文件

你可以运行`make debug`与`make clean`或者其他任何Makefile命令。

```
$ make config
$ make build
```

**4.** 启动MatrixOne服务

```
$ ./mo-server system_vars_config.toml
```
#### 下载二进制包
 从0.3.0版本开始，您可以直接下载二进制包，然后在X86_64 Linux环境中运行MatrixOne。  
**1.** 下载二进制包并解压
 ```
 $ wget https://github.com/matrixorigin/matrixone/releases/download/v0.3.0/mo-server-v0.3.0-linux-amd64.zip
 $ unzip mo-server-v0.3.0-linux-amd64.zip
 ```

 **2.** 启动MatrixOne服务
 ```
 $./mo-server system_vars_config.toml
 ```


#### 使用docker

1. 安装docker

请检查Docker daemon是否正在后台运行，并确认docker版本：
```
$ docker --version
```
2. 创建并运行容器

使用以下命令将从Docker Hub中拉取最近的MatrixOne镜像：
```
$ docker run -d -p 6001:6001 --name matrixone matrixorigin/matrixone:latest
```
### 🌟 连接MatrixOne服务

1. 安装MySQL客户端
   
  MatrixOne支持MySQL连接协议，因此您可以使用各种语言通过MySQL客户机程序进行连接。  
  目前，MatrixOne只兼容Oracle MySQL客户端，因此一些特性可能无法在MariaDB、Percona客户端下正常工作。  



2. 连接MatrixOne服务

你可以使用MySQL命令行客户端来连接MatrixOne服务。  

```
$ mysql -h IP -P PORT -uUsername -p
```
连接符的格式与MySQL格式相同，您需要提供用户名和密码。  
此处以内置帐号作为示例：  

   - user: dump
   - password: 111

```
$ mysql -h 127.0.0.1 -P 6001 -udump -p
Enter password:
```

目前，MatrixOne只支持TCP监听。




## 🙌 <a id="contributing">参与贡献</a>

欢迎大家对MatrixOne的贡献。  
请查看[贡献指南](https://docs.matrixorigin.io/cn/0.3.0/MatrixOne/Contribution-Guide/make-your-first-contribution/)来了解有关提交补丁和完成整个贡献流程的详细信息。

### 👏贡献者们
<br><!-- Do not remove start of hero-bot -->
<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/wanhanbo"><img src="https://avatars.githubusercontent.com/u/97089788?v=4?s=100" width="100px;" alt=""/><br /><sub><b>wanhanbo</b></sub></a><br /><a href="https://github.com/wanhanbo/mytest/issues?q=author%3Awanhanbo" title="Bug reports">🐛</a></td>
    <td align="center"><a href="https://github.com/dengn"><img src="https://avatars.githubusercontent.com/u/4965857?v=4?s=100" width="100px;" alt=""/><br /><sub><b>dengn</b></sub></a><br /><a href="https://github.com/wanhanbo/mytest/issues?q=author%3Adengn" title="Bug reports">🐛</a> <a href="https://github.com/wanhanbo/mytest/commits?author=dengn" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
<!-- Do not remove end of hero-bot --><br>


<!-- Do not remove end of hero-bot --><br>

## <a id="license">License</a>
[Apache License, Version 2.0](LICENSE).

