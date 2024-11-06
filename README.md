# 使用说明

## 安装所需依赖

```sh
pnpm add ssh2 dotenv -D
```

## 添加 scripts 指令

在 `package.json` 文件中添加 `deploy` 指令

```json
{
	"scripts": {
		// node 执行入口脚本路径根据实际调整
		"deploy": "node ./index.js"
	}
}
```

## 添加环境变量

1. 在项目根目录下创建 `.env` 文件，添加以下环境变量

```sh
SSH_HOST='xxx.xx.xx.xxx'
SSH_PORT=22
SSH_USERNAME=xxx
SSH_PASSWORD=xxx
```

2. 同时添加 `.env.example` 文件，方便其他开发者参考所需环境变量

```sh
SSH_HOST=
SSH_PORT=22
SSH_USERNAME=
SSH_PASSWORD=
```

3. 在 `.gitignore` 文件中添加 `.env` 文件，避免将环境变量文件提交到远程仓库

## 运行部署

```sh
pnpm run deploy
```

## 待办事项

- 服务端部署，优化多文件上传
- 支持 Github 部署
