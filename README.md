# SAM应用示例

这是一个由AWS SAM（Serverless Application Model）创建的简单Hello World应用程序。

## 部署说明

### 前提条件

* AWS CLI已安装并配置
* SAM CLI已安装
* Python 3.11

### 构建和部署

```bash
# 构建应用
sam build

# 部署应用
sam deploy --guided
```

### 测试应用

部署成功后，您可以通过输出中提供的API Gateway端点URL来访问应用程序：

```
https://[api-id].execute-api.[region].amazonaws.com/Prod/hello/
```

## 本地开发和测试

```bash
# 本地调用Lambda函数
sam local invoke

# 本地启动API网关
sam local start-api
```

## 项目结构

```
.
├── README.md           # 项目文档
├── events/             # 测试事件
├── hello_world/        # Lambda函数代码
│   ├── __init__.py
│   ├── app.py          # Lambda处理函数
│   └── requirements.txt # Python依赖
├── samconfig.toml      # SAM配置文件
├── template.yaml       # SAM模板文件
└── tests/              # 测试代码
```