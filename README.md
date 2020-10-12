# spec
> 开发套路

## 开发规范 业务驱动 业务流程
> * 先定义业务泳道图  系统原型持续维护
> * PRD文档

## 开发规范 测试驱动 测试用例定义
> * 先定义业务测试用例, 开发人员依照测试用例进行开发
> * 开发质量 benchmark: 测试到问题提交到 github issue, 不通过测试用例测试影响绩效（自动化统计), 自行测试

## 开发规范 领域驱动逻辑原型开发
> * 定义数据库设计原型, 关系字段包括 [id, name, data{json}, status, owner_id, queue_id，...]
> * 首先进行核心逻辑的开发业务原型，定义业务层sql查询任务列表


## 开发规范 接口预定义 前端界面对接优先
> *  开发人员可进行详细的数据库实体设计，并由[dev-cli/dbToCrudless.py](https://github.com/kequandian/dev-cli/blob/master/dbToCrudless.py)脚本生成基础配置文件 crudless.yml
> *  依据项目业务流程图以及原型，开发人员以及测试人员均可预定义api返回字段 [Record, Model]，首先完成前端对接


## 开发规范 CRUD 高度可配置化实施
> * 通过 excel 定义菜单操作以及字段列表 (转换为  crudless.yml)
> * 在excel表中定义明确的操作流程


## 开发规范 系统框架支持插件开发
> * CRUD 
> * 

## 开发规范 标准库化开发 提供Sandbox
> * 全自治开发，可独立测试，可独立部署，提供api文档，提供完整的使用说明, 关联前端代码地址
> * 支持 sandbox 热装配组件部署

## 开发规范 权限可配置 由excel提供说明
> * 权限可由  crudless.yml 配置
> * 权限可通过 excel 表生成 crudless.yml 配置, 前端框架可响应crudless.yml 配置

## 开发规范  准备测试数据
> * 测试数据[通常为 sql语句]，作为项目代码提交
> * 提供独立测试数据 sandbox, 独立运行独立greenfield初始化

## 开发规范  实时响应  
> * 开发过程中对实体字段的修改 通过修改 -schema.sql，实时响应到界面（自动化方案）
> * 前端框架支持在线编辑，自动同步代码与效果， 可变更字段, 操作, 详情

## 开发规范  生产环境部署全自动化 
> * 生产环境提交至部署  （提交代码，则自动化完成）
> * 通过 jenkins, archiva 实现半自动化
> * 运营环境 工人测试通过  工人触发部署到运营环境  (仅针对运营中的重要项目）
> * app-schedule等需独立模块，仅由生产环境**standalone**依赖

## 开发规范 服务监控
> * 对服务器进行有效管理，充分利用 prometheus agent + sandbox 对每台服务器性能进行监控
