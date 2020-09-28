# spec


## 开发规范  业务驱动
> 先定义业务泳道图  系统原型持续维护


## 开发规范  测试驱动
> 先定义测试用例,  独立服务可测试,  基于服务单元 sandbox 进行测试,  使 sandbox 可简易组合


## 开发规范 CRUD接口
> * 由 crudless.yml 定义 (提供逆向转换=>由 前端配置生成  crudless.yml 配置）
> * 下一步可通过 excel 定义，转换为  crudless.yml
> * 代码级别先提供 Record, Model 实体定义，优先对接前端框架


## 开发规范 权限可配置
> * 权限可由  crudless.yml 配置
> * 权限可通过 excel 表生成 crudless.yml 配置, 前端框架可响应crudless.yml 配置


## 开发规范  实时响应
> * 开发过程中对实体字段的修改 可实时响应到界面  （自动化方案）
> * 前端框架如何处理配置文件更新 与 代码更新的问题 
> > * 前端框架插件化，命名化，通过组件命名，组件独立js文件


## 开发规范  数据库同步
> 代码 resources/sql/-schema.sql 的修改 自动触发 与数据库的同步  （提供 maven 插件自动同步）
> 大面积修改可进行 greenfield, 重新导入数据  （先导出数据, greenfield 完成后，重新导入数据)
> 提交最挂实践
