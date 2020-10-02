# spec


## 开发规范 业务驱动
> 先定义业务泳道图  系统原型持续维护


## 开发规范 测试驱动
> 先定义业务测试用例, 开发人员依照测试用例进行开发, 测试到问题提交到 github issue.  开发质量 benchmark


## 开发规范 领域驱动
> * 定义数据库设计原型, 关系字段包括 [id, name, data{json}, status, owner_id, queue_id，...], 明确区分**数据流**与**查询隔离**
> * 详细测试业务原型，定义业务层sql查询任务列表


## 开发规范 CRUD配置实施
> * 由 crudless.yml 定义 (提供逆向转换=>由 前端配置生成  crudless.yml 配置）
> * 下一步可通过 excel 定义，转换为  crudless.yml
> * 代码级别先提供 Record, Model 实体定义，优先对接前端框架

## 开发规范  领域开发
> * 基于领域驱动原型进行开发


## 开发规范 标准库与测试数据
> * 对于标准化开发，如uaas, 需保留或提供测试数据用于举例测试，如角色管理 [客服角色]测试数据, 订单管理 [计划，预约]的角色测试数据
> * 订单原型，客服原型，逻辑关闭，字段开放


## 开发规范 权限可配置
> * 权限可由  crudless.yml 配置
> * 权限可通过 excel 表生成 crudless.yml 配置, 前端框架可响应crudless.yml 配置


## 开发规范  实时响应
> * 开发过程中对实体字段的修改 可实时响应到界面  （自动化方案）
> * 前端框架如何处理配置文件更新 与 代码更新的问题 
> > * 前端框架插件化，命名化，通过组件命名，组件独立js文件


## 开发规范  数据库同步
> * 代码 resources/sql/-schema.sql 的修改 自动触发 与数据库的同步  （提供 maven 插件自动同步）
> * 大面积修改可进行 greenfield, 重新导入数据  （先导出数据, greenfield 完成后，重新导入数据)
> * 提交最挂实践


## 开发规范  服务组件标准化
> * 如 系统管理 需要标准化,  有固定的代码维护git 地址, 包括前后端
> * 支持 sandbox 热装配组件部署


## 开发规范  生产环境部署全自动化 
> * 生产环境提交至部署  （提交代码，则自动化完成）
> * 通过 jenkins, archiva 实现半自动化
> * 运营环境 工人测试通过  工人触发部署到运营环境  (仅针对运营中的重要项目）



