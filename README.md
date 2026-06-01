# deepseek_1.5b_deploy_attempt
记录DeepSeek 1.5B模型本地部署的大概过程
# DeepSeek 1.5B 本地部署记录

## 实验环境
- 硬件：机械革命旷世16笔记本，CPU i5-134500h/ 内存 32G / 4050 6G
- 系统：Windows 11 24H2
- 工具：Ollama

## 部署过程
1. 在 WSL2 中安装 Ollama
   curl -fsSL https://ollama.com/install.sh | sh
2. 拉取模型
   ollama pull deepseek-r1:1.5b
3. 运行对话测试
   ollama run deepseek-r1:1.5b
   >>> 你好，请介绍一下自己

## 当时遇到的问题和解决
- 问题：第一次运行时提示内存不足
- 排查：WSL2 默认只分配了4G内存
- 解决：在用户目录下新建 .wslconfig 文件，将内存上限调到8G

## 效果回忆
1.5B模型推理速度可以接受，简单对话基本流畅，但复杂逻辑推理拉完了 讲笑话都费劲
