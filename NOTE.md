### workflow注解

- 整个流程在master分支发生push事件时触发。
- 只有一个job，运行在虚拟机环境ubuntu-latest。
- 第一步是获取源码，使用的 action 是actions/checkout。
- 第二步是构建和部署，使用的 action 是JamesIves/github-pages-deploy-action。
- 第二步需要四个环境变量，分别为 GitHub 密钥、发布分支、构建成果所在目录、构建脚本。其中，只有 GitHub 密钥是秘密变量，需要写在双括号里面，其他三个都可以直接写在文件里。