### Release v1.1

2018.09.19

- command 命令支持变量占位符 `{{file}}`、`{{ext}}`、`{{changed}}`；  

```yaml
# {{file}}    文件名(如 a.txt 、test/test2/a.go)
# {{ext}}     文件后缀(如 .go)
# {{changed}} 文件更新的本地时间戳(纳秒,如 1537326690523046400)
# 变量占位符使用示例：cp {{file}} /root/sync -rf  、 myCommand --{{ext}} {{changed}}
```

- 增加 较深目录递归提示；  
- 优化 文字提示；  
- 修复 command 命令执行时目录不正确的问题； 
- 修复 其他bug; 



### Release v1.0

2018.09.10

- 文件变更监听支持多平台 （windows/linux测试，mac未测试）；  

- 支持灵活配置监听 包含文件夹/排除文件夹/特定文件类型；  

- 支持配置变更要运行命令，可以有多条，会依次执行；  

- 支持 fileboy init 初始化配置，生成 filegirl.yaml 文件；  

- 支持 fileboy exec 直接执行配置的 command 命令；  