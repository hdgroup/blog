---

layout: post
title: Java Roadmap
categories: Java
description: Java
keywords: Java

---

# 多线程与高并发
进程、线程、协程  
并行、并发  
同步、异步  
死锁、饥饿、活锁  
线程安全  
Java内存模型 Java Memory Model JMM  
创建线程的三种方式  
1 继承 Thread 类  
2 实现 Runnable 接口  
3 使用线程池  
线程的状态 new、ready、running、block、dead  

synchronized、ReentrantLock  
Semaphore、CountDownLatch、CyclicBarrier、Condition  
Callable、Future  


# 缓存
缓存穿透、缓存击穿、缓存雪崩  
## Redis
跳表  

## Caffeine

# 大Key
工具 rdb_bigkeys  

# 算法

# 分布式系统的一致性
zookeeper  
拜占庭将军问题  
paxos raft  

# 分布式事务
Seata

# 状态机

# More
- [https://github.com/alibaba/canal](https://github.com/alibaba/canal)
