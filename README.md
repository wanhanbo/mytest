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
  <a href="https://github.com/matrixorigin/matrixone/blob/main/README.cn.md">
    <b>简体中文</b>
  </a>
</div>


<h3 align="center">Connect with us:</h3>
<p align="center">
<a href="https://twitter.com/matrixone16" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="matrixone16" height="30" width="40" /></a>
<a href="http://matrixoneworkspace.slack.com" target="blank"><img align="center" src="https://github.com/dengn/CASAUVSQ/blob/priority/slack_icon.png" alt="matrixone16" height="30" width="30" /></a>

</p>




Contents
========

* [What is MatrixOne](#what-is-matrixone)
* [KeyFeatures](#key-features)
* [User Values](#user-values)
* [Architecture](#architecture)
* [Quick start](#quick-start)
* [Contributing](#contributing)
* [License](#license)

## What is MatrixOne?



MatrixOne is a future-oriented hyper-converged cloud and edge native DBMS that supports transactional, analytical, and streaming workloads with a simplified and distributed database engine, across multiple data centers, clouds, edges and other heterogeneous infrastructures.


##  🎯 <a id="key-features">Key Features</a> 
### 💥 **Hyper-converged Engine**
* **Monolithic Engine**
  
     A monolithic database engine is designed to support hybrid workloads: transactional, analytical, streaming, time-series, machine learning, etc.

* **Built-in Streaming Engine**
  
     With the built-in streaming engine, MatrixOne supports in-database streaming processing by groundbreaking incremental materialized view maintenance.

### ☁️ **Cloud & Edge Native**
* **Real Infrastructure Agnostic**
  
     MatrixOne supports seemless workload migration and bursting among different locations and infrastructures.

* **Multi-site Active/Active**
  
     MatrixOne provides industry-leading latency control with optimized consistency protocol.

### 🚀 **Extreme Performance**
* **High Performance**
  
     Accelerated queries supported by patented vectorized execution as well as optimal computation push down strategies through factorization techniques.

* **Strong Consistency**
  
     MatrixOne introduces a global, high-performance distributed transaction protocol across storage engines.

* **High Scalability**
  
     Seamless and non-disruptive scaling by disaggregated storage and compute.   
## 💎 **<a id="user-values">User Values</a>**
<details>
  <summary><b><font size=4>Simplify Database Management and Maintenance</b></font></summary> 
     To solve the problem of high and unpredictable cost of database selection process, management and maintenance due to database overabundance, MatrixOne all-in-one architecture will significantly simplify database management and maintenance, single database can serve multiple data applications.
</details>
<details>
  <summary><b><font size=4>Reduce Data Fragmentation and Inconsistency</b></font></summary>
     Data flow and copy between different databases makes data sync and consistency increasingly difficult. The unified incrementally materialized view of MatrixOne makes the downstream can support real-time upstream update, achieve the end-to-end data processing without redundant ETL process.
</details>
<details>
  <summary><b><font size=4>Decoupling Data Architecture From Infrastructure</b></font></summary>
     Currently the architecture design across different infrastructures is complicated, causes new data silos between cloud and edge, cloud and on-premise. MatrixOne is designed with unified architecture to support simplified data management and operations across different type of infrastructures.
</details>
<details>
  <summary><b><font size=4>Extremely Fast Complex Query Performance</b></font></summary>  
     Poor business agility as a result of slow complex queries and redundant intermediate tables in current data warehousing solutions. MatrixOne  supports blazing fast experience even for star and snowflake schema queries, improving business agility by real-time analytics.
</details>
<details>
  <summary><b><font size=4>A Solid OLTP-like OLAP Experience</b></font></summary>   
     Current data warehousing solutions have the following problems such as high latency and absence of immediate visibility for data updates. MatrixOne brings OLTP (Online Transactional Processing) level consistency and high availability to CRUD operations in OLAP (Online Analytical Processing).
</details>
<details>
  <summary><b><font size=4>Seamless and Non-disruptive Scalability</b></font></summary>   
     It is difficult to balance performance and scalability to achieve optimum price-performance ratio in current data warehousing solutions. MatrixOne's disaggregated storage and compute architecture makes it fully automated and efficient scale in/out and up/down without disrupting applications.
</details>

<br>


## 🔎 <a id="architecture">Architecture</a>
MatrixOne consists of multiple components and form a complete system.  
The architecture is as follows:   
<p align="center">
  <img alt="MatrixOne" height="500" width="700" src="https://github.com/matrixorigin/artwork/blob/main/docs/overview/overall-architecture.png?raw=true">
</p>
<details>
  <summary><font size=4 style=IT><b>Query Parser Layer</b></font></summary>

   **Parser**: Parses SQL, Streaming Query, or Python language into an abstract syntax tree for further processing.  

   **Planner**: Finds the best execution plan through rule-based, cost-based optimization algorithms, and transfers abstract syntax tree to plan tree.  

   **IR Generator**: Converts Python code into an intermediate representation.
</details>  

<details>
  <summary><font size=4 style=IT><b>Computation Layer</b></font></summary>

   **JIT Compilation**: Turns SQL plan tree or IR code into a native program using LLVM at runtime.  

   **Vectorized Execution**: MatrixOne leverages SIMD instructions to construct vectorized execution pipelines.  

   **Cache**: Multi-version cache of data, indexes, and metadata for queries.
</details>
  
<details>
  <summary><font size=4 style=IT><b>Cluster Management Layer</b></font></summary>

MatrixCube is a fundamental library for building distributed systems, which offers guarantees about reliability, consistency, and scalability. It is designed to facilitate distributed, stateful application building to allow developers only need to focus on the business logic on a single node.  
MatrixCube is currently built upon multi-raft to provide replicated state machine and will migrate to Paxos families to increase friendliness to scenarios spanning multiple data centers.
   **Prophet**: Used by MatrixCube to manage and schedule the MatrixOne cluster.  
   **Transaction Manager**: MatrixOne supports distributed transaction of snapshot isolation level.  
   **Replicated State Machine**: MatrixOne uses RAFT-based consensus algorithms and hybrid logic clocks to implement strong consistency of the clusters. Introduction of more advanced state-machine replication protocols is yet to come.
For detailed information about **MatrixCube**, you can see [MatrixCube Tech Design](https://docs.matrixorigin.io/0.3.0/MatrixOne/Overview/matrixcube/matrixcube-introduction/)
</details>

<details>
  <summary><font size=4 style=IT><b>Replicated Storage Layer</b></font></summary>

   **Row Storage**: Stores serving workload, metadata, and catalog.  
   **Column Storage**: Stores analytical workload and materialized views.
</details>

<details>
  <summary><font size=4 style=IT><b>Storage Provision Layer</b></font></summary>

  MatrixOne stores data in shared storage of S3 / HDFS, or the local disk, on-premise server, hybrid and any cloud, or even smart devices.
</details>
<br>

**[MatrixOne Tech Design](https://docs.matrixorigin.io/0.3.0/MatrixOne/Overview/MatrixOne-Tech-Design/matrixone-techdesign/)** may help you to understand the architecture of MatrixOne.

## ⚡️ <a id="quick-start">Quick start</a>
Get started with MatrixOne quickly by the following steps.
### ⚙️ Install MatrixOne
MatrixOne supports Linux and MacOS. You can install MatrixOne either by [building from source](#building-from-source) or [using docker](#using-docker).
#### **Building from source**

1. Install Go (version 1.17 is required).
  
2. Get the MatrixOne code:

```
$ git clone https://github.com/matrixorigin/matrixone.git
$ cd matrixone
```

3. Run make:

You can run `make debug`, `make clean`, or anything else our Makefile offers.

```
$ make config
$ make build
```

4. Boot MatrixOne server:

```
$ ./mo-server system_vars_config.toml
```

#### **Downloading binary packages**

Starting with 0.3.0, you can download binary packages directly to run MatrixOne in the X86_64 Linux environment.

1. Download binary packages and decompress

```
$ wget https://github.com/matrixorigin/matrixone/releases/download/v0.3.0/mo-server-v0.3.0-linux-amd64.zip
$ unzip mo-server-v0.3.0-linux-amd64.zip
```

2. Launch MatrixOne server

```
$./mo-server system_vars_config.toml
```

#### **Using docker**

1. Install Docker, then verify that Docker daemon is running in the background:

```
$ docker --version
```
2. Create and run the container for the latest release of MatrixOne. It will pull the image from Docker Hub if not exists.
   
```
$ docker run -d -p 6001:6001 --name matrixone matrixorigin/matrixone:latest
```
### 🌟 Connecting to MatrixOne server

1. Install MySQL client.
   
   MatrixOne supports the MySQL wire protocol, so you can use MySQL client drivers to connect from various languages. Currently, MatrixOne is only compatible with Oracle MySQL client. This means that some features might not work with MariaDB client.

2. Connect to MatrixOne server:

```
$ mysql -h IP -P PORT -uUsername -p
```
   The connection string is the same format as MySQL accepts. You need to provide a user name and a password. 

   Use the built-in test account for example:

   - user: dump
   - password: 111

```
$ mysql -h 127.0.0.1 -P 6001 -udump -p
Enter password:
```

Now, MatrixOne only supports the TCP listener. 




## 🙌 <a id="contributing">Contributing</a>

Contributions to MatrixOne are welcome from everyone.  
 See [Contribution Guide](https://docs.matrixorigin.io/0.3.0/MatrixOne/Contribution-Guide/make-your-first-contribution/) for details on submitting patches and the contribution workflow. 

### 👏 All contributors
<br><!-- Do not remove start of hero-bot -->
<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/wanhanbo"><img src="https://avatars.githubusercontent.com/u/97089788?v=4?s=100" width="100px;" alt=""/><br /><sub><b>wanhanbo</b></sub></a><br /><a href="https://github.com/wanhanbo/mytest/issues?q=author%3Awanhanbo" title="Bug reports">🐛</a></td>
    <td align="center"><a href="https://github.com/dengn"><img src="https://avatars.githubusercontent.com/u/4965857?v=4?s=100" width="100px;" alt=""/><br /><sub><b>dengn</b></sub></a><br /><a href="https://github.com/wanhanbo/mytest/issues?q=author%3Adengn" title="Bug reports">🐛</a> <a href="https://github.com/wanhanbo/mytest/commits?author=dengn" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/domingozhang"><img src="https://avatars.githubusercontent.com/u/88298673?v=4?s=100" width="100px;" alt=""/><br /><sub><b>DomingoZhang</b></sub></a><br /><a href="https://github.com/wanhanbo/mytest/commits?author=domingozhang" title="Documentation">📖</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
<!-- Do not remove end of hero-bot --><br>

## <a id="license">License</a>
MatrixOne is licensed under the [Apache License, Version 2.0](LICENSE).


