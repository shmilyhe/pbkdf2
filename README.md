# 简介

pbkdf2 是一个比较流行的密钥算法，在国内gogs 项目密钥就采有用了这个算法。但在jdk 内置只实现了PBKDF2WithHmacSHA1，其它的组合的支持并不善。查阅了大量相关的文档后借鉴了gogs 的代码用java 实现了相对完整的API

示例：
```
    /**
		 * gogs 采用的密钥算法
		 */
		System.out.println(PBKDF2.pbkdf2("Admin","4wcsVGKRvi",10000,50,new Sha256()));
```
