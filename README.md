# 中文简体版--唐宋诗词集
基于chinese-poetry词库整理的一份mysql资源库
# 原库地址
https://github.com/chinese-poetry/chinese-poetry.git
# 表机构说明
## 表结构说明
```sql
#####唐宋诗数据表
create table poetry (
  id int(11) not null primary key auto_increment,
  author_id int(11) default 0,
  title varchar(255) not null,
  content text not null,
  yunlv_rule text default null,
  author varchar(255) not null,
  dynasty char(1) not null
) engine = myisam, charset=utf8;

#####唐宋诗作者数据表
create table poetry_author (
  id int(11) not null primary key auto_increment,
  name varchar(255) not null,
  intro text default null,
  dynasty char(1) not null
) engine = myisam, charset=utf8;

#####宋词作者数据表
create table poems_author (
  id int(11) not null primary key auto_increment,
  name varchar(255) not null,
  intro_l text default null,
  intro_s text default null
) engine = myisam, charset=utf8;

#####宋词数据表
create table poems (
  id int(11) not null primary key auto_increment,
  author_id int(11) default 0,
  title varchar(255) not null,
  content text not null,
  author varchar(255) not null
) engine = myisam, charset=utf8;

#####论语数据表
create table lunyu (
  id int(11) not null primary key auto_increment,
  chapter varchar(255) not null,
  content text not null
) engine = myisam, charset=utf8;

#####诗经数据表
create table shijing (
  id int(11) not null primary key auto_increment,
  title varchar(255) not null,
  chapter varchar(255) not null,
  section varchar(255) not null,
  content text not null
) engine = myisam, charset=utf8;
```
