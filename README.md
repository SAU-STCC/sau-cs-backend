# sau-cs-backend
sau-cs-backend

## 数据库设计

~~~sql
CREATE TABLE `articles` (
  `id` int(10) unsigned NOT NULL auto_increment, -- 文章 ID
  `title` varchar(150) default NULL, -- 文章标题
  `slug` varchar(150) default NULL, -- 文章别名
  `created` int(10) unsigned default '0', -- 创建时间
  `modified` int(10) unsigned default '0', -- 上次修改时间
  `text` longtext, -- 文章内容
  `order` int(10) unsigned default '0', -- 排序
  `authorId` int(10) unsigned default '0', -- 作者 ID
  `template` varchar(32) default NULL, -- 模板
  `type` varchar(16) default 'post', -- 类型
  `status` varchar(16) default 'publish', -- 状态
  `password` varchar(32) default NULL, -- 访问密码
  `commentsNum` int(10) unsigned default '0', -- 评论数
  `allowComment` char(1) default '0', -- 是否允许评论
  `allowPing` char(1) default '0', -- 允许被引用
  `allowFeed` char(1) default '0', -- 允许聚合中出现
  `parent` int(10) unsigned default '0',
  PRIMARY KEY  (`cid`),
  UNIQUE KEY `slug` (`slug`),
  KEY `created` (`created`)
) ENGINE=%engine%  DEFAULT CHARSET=%charset%;
~~~

## API










