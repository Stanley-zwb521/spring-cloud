###############################
ELK
###############################

ELK Stack是三个开源产品的集合--Elasticsearch、Logstash和Kibana。它们都是由Elastic公司开发、管理和维护。

Elasticsearch是实时全文搜索和分析引擎，提供搜集、分析、存储数据3大功能；是一套开放REST和JAVA API等结构提供高效搜索功能，可扩展的分布式系统。它构建于Apache Lucene搜索引擎库之上。
 
Logstash是一个用来搜集、分析、过滤日志的工具。它支持几乎任何类型的日志，包括系统日志、错误日志和自定义应用程序日志。它可以从许多来源接收日志，这些来源包括 syslog、消息传递（例如 RabbitMQ）和JMX，它能够以多种方式输出数据，包括电子邮件、websockets和Elasticsearch。
 
Kibana是一个基于Web的图形界面，用于搜索、分析和可视化存储在 Elasticsearch指标中的日志数据。它利用Elasticsearch的REST接口来检索数据，不仅允许用户创建他们自己的数据的定制仪表板视图，还允许他们以特殊的方式查询和过滤数据
 
ELK 的设计目的是让用户能够从任何来源、任何格式的数据中获取数据，并对这些数据进行实时搜索、分析和可视化。

ELK提供了集中式的日志记录，当试图识别服务器或应用程序的问题时，它非常有用。它允许您在一个地方搜索所有的日志。它还可以通过连接多个服务器的日志，在特定的时间框架内连接它们的日志，帮助查找多个服务器中发生的问题。

ELK的架构图
===============
.. image:: images/elk-01.png
   :alt: alternate text


Elasticsearch
===========================


Logstash
===========================


Kibana
===========================

参考
========
#. https://www.guru99.com/elk-stack-tutorial.html
#. https://elkguide.elasticsearch.cn/
#. https://github.ibm.com/lanzejun/elk
#. https://www.hz20180220.xin/centos-7-x-bu-shu-elk/