<<<<<<< HEAD
## 1.go mod 管理依赖

```shell
go mod init gitee.com/RandyField/GinForOAuth
go get -u github.com/gin-gonic/gin
```

## 2.编码

```go
package main

import (
	"net/http"

	"github.com/gin-gonic/gin"	
)

func main() {
	r := gin.Default()
	r.GET("/", func(c *gin.Context) {
		c.JSON(http.StatusOK, gin.H{
			"message": "hello,go-gin wholeheartedly at your service",
		})
	})

	
	r.Run() // listen and serve on 0.0.0.0:8080 (for windows "localhost:8080")
}
```

## 3.启动

```shell
go run main.go
```

## 4.git关联远程库

```shell
git init
git remote add origin git@gitee.com:RandyField/GinForOAuth.git
git push -u origin master

 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to ''
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

#把远程仓库和本地同步，消除差异
git pull origin master --allow-unrelated-histories 

git add -A
git commit -m "[dev]init"
git push -u origin master
```



=======
# GinForOAuth
>>>>>>> 6ca29cf31a52dfed5c28042b702d5f3926a97908
