## 安装tendermint 
### 1. 下载源代码 到 $GOPATH/src/github.com/tendermint 目录下
git clone https://github.com/tendermint/tendermint.git

### 2.进入tendermint目录
cd tendermint/

### 3. 执行 make get_tools

### 4. 执行 make get_vendor_deps

提示：

  ✗ unable to deduce repository and source type for "google.golang.org/grpc": unable to read metadata: unable to fetch raw metadata: failed HTTP request to URL "http://google.golang.org/grpc?go-get=1": Get http://google.golang.org/grpc?go-get=1: dial tcp 216.239.37.1:80: connect: connection refused
  ✗ unable to deduce repository and source type for "golang.org/x/net": unable to read metadata: unable to fetch raw metadata: failed HTTP request to URL "http://golang.org/x/net?go-get=1": Get http://golang.org/x/net?go-get=1: dial tcp 216.239.37.1:80: connect: connection refused

解决方法：
修改Gopkg.toml 

[[override]]
  name = "golang.org/x/net"
  source = "https://github.com/golang/net.git"

[[override]]
  name = "google.golang.org/grpc"
  source = "https://github.com/grpc/grpc-go.git"
  
  
  
  
