# elm-test-report
TJU-ELM 外卖平台接口测试报告
# 外卖平台接口测试报告

## 测试环境
- 操作系统：Windows 10
- 后端：SpringBoot 2.x，运行端口 8080
- 前端：Vue3，运行端口 8081
- 数据库：MySQL 8.0
- 测试工具：Apifox

## 测试范围
| 接口名称 | 方法 |网站| 测试内容 |
|---------|------|-----|----------|
| 获取商家列表 | POST | /BusinessController/listBusinessByOrderTypeId | 传入 orderTypeId=1，验证返回商家数组 |
| 根据ID查询用户 | POST | /UserController/getUserById | 传入 userId=1，验证返回正确的用户信息 |

## 测试结果
- ✅ 获取商家列表：通过（状态码200，返回商家数据数组，长度>0）
- ✅ 根据ID查询用户：通过（状态码200，返回 userId=1 的用户对象）

## 断言配置
- 响应状态码必须为 200
- 商家列表接口：响应体数组长度 > 0
- 查询用户接口：响应体中的 userId 字段等于请求的 userId

## 测试报告文件
- [点击查看完整报告](./test-report.md)

## 截图
（可选，粘贴接口请求/响应的截图）
![商家列表接口](./screenshot1.png)
![查询用户接口](./screenshot2.png)

## 结论
核心接口功能正常，测试通过。登录接口发现缺陷（密码验证异常），已单独记录。
