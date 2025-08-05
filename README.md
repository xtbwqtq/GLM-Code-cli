## GLM-Code-cli

本项目基于对Gemini cli的分支，添加了对于OpenAI格式的兼容，尤其是GLM-4.5。

项目兼容了Gemini cli的所有特性，包括流式输出，工具调用，中断，上下文压缩等等。

有问题欢迎提问。

## 使用

首先需要node 20以上

打开你的project，启动终端

### 📢：Gemini默认是开启了遥测的，我们整个场景不需要，因此需要关闭

遥测会请求谷歌的服务。

可以在当前project目录新建`.gemini`目录，然后设置setting.json文件,telemetry 是遥测相关的：
```
{
  "theme": "Google Code",
  "usageStatisticsEnabled": false,
  "telemetry": {
    "enabled": false,
    "logPrompts": false
  }
}
```

### 命令

1 设置OpenAI的环境变量

linux|Mac：
```
export OPENAI_API_KEY="xxxx"
export OPENAI_BASE_URL="xxxxx"
```
Windows power shell：
```
$env:OPENAI_API_KEY="xxxx"
$env:OPENAI_BASE_URL="xxxxx"
```

比如：
```
export OPENAI_API_KEY="bffed1xxxxxxxx"
export OPENAI_BASE_URL="https://open.bigmodel.cn/api/paas/v4/"
```

运行
```
node [gemini.js] --model model_name
```

示例：

```
node /Users/pan/2022workspace/gemini.js --model glm-4.5-flash
```

初次运行选择：`openai-api-key` 的认证方式。
<img width="901" height="360" alt="image" src="https://github.com/user-attachments/assets/159049b3-9171-451d-9858-d224eff172d0" />

运行成功之后：
<img width="939" height="411" alt="image" src="https://github.com/user-attachments/assets/5fd2fcdb-99be-459a-9aa9-49f55b8a6fb1" />



