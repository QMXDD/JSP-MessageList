# JSP-MessageList
使用DAO模式来实现简单的论坛留言板功能
    大三的java web课程的实验内容，主要是通过DAO模式来对MVC模式进行扩展。
    包括用户功能和管理员功能
    用户功能包括：注册、登录、查看所有留言、查看我的留言、查看留言详情、写留言、设置私密留言、点赞留言、评论留言、按留言标题模糊查找、查看某个用户的所有留言、查看个人注册信息。
    管理员功能包括：删除用户、冻结用户使其不能登录、解冻用户使其可以登录、删除留言、删除评论。
    
    数据库设计如下：
    创建一个数据库，命名为实验。
    其中包括三个表：用户信息表、留言信息表、评论信息表。
    用户表结构如下：
    `name` varchar(20) NOT NULL,
    `password` varchar(20) NOT NULL,
    `gender` varchar(10) DEFAULT NULL,
    `degree` varchar(20) DEFAULT NULL,
    `hobby` varchar(30) NOT NULL,
    `email` varchar(30) DEFAULT NULL,
    `introduction` varchar(200) DEFAULT NULL,
    `status` varchar(1) NOT NULL,
    PRIMARY KEY (`name`)
    留言表结构如下：
    `title` varchar(20) NOT NULL,
    `context` varchar(200) NOT NULL,
    `author` varchar(20) NOT NULL,
    `time` varchar(50) DEFAULT NULL,
    `view` int(11) DEFAULT NULL,
    `good` int(11) NOT NULL,
    `visio` varchar(2) NOT NULL,
    PRIMARY KEY (`context`),
    KEY `FK_NAME` (`author`)
    评论信息表结构如下：
    `title` varchar(20) NOT NULL,
    `content` varchar(50) NOT NULL,
    `author` varchar(20) NOT NULL,
    `time` varchar(50) NOT NULL
