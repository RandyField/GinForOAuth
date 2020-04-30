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
```



