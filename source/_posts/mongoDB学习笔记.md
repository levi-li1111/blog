# mongoDB 学习笔记

## 数据库相关

- show dbs
- dbs

## 概念

- 集合 >> 表
- 文档记录 >> 记录

## SQL语句

- use mydb -- 切换/创建数据库
- db.dropDatabase() mydb -- 删除当前数据库  删库跑路
- db.student.insert({"id": 1,"name": "张三","age": 28}) 新增表及数据
- db.student.insertOne
- db.student.insert
- db.student.insertMany
- db.student.drop() 删除集合student
- db.student.find().pretty() -- 查找所有
- db.student.find({"age": 1}).pretty() -- 查找符合条件的
- db.student.find().limit(10).skip(10) -- 分页查找
- db.student.find().sort({"age": 1}) -- 排序 1 升序， -1 降序
- db.student.find().count() -- count() 聚合
- db.student.update({"name": "小明"}, {$set:{"age": 16}) -- 更新匹配一个
- db.student.update({"name": "小明"}, {$set:{"age": 16}},{multi: true}) -- 更新匹配的所有
- db.student.update({"name": "小明"}, {"age": 16, "name":"王五", "age": 39}) -- 文档替换
- db.student.remove({"name":"小明"})   -- 删除 所有匹配记录
- db.student.remove({"name":"小明"},{justOne, true}) -- 进删除一条

## 索引

