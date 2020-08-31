我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

# App

A sample 12 Facter Application.

## Usage

Download:

```
mkdir $GOPATH/src/github.com/kelseyhightower
cd $GOPATH/src/github.com/kelseyhightower 
git clone https://github.com/kelseyhightower/app.git
```

Generate TLS certificates:

```
$ go run certgen/main.go
```
```
wrote ca.pem
wrote ca-key.pem
wrote server.pem
wrote server-key.pem
```

### Build and Run

```
$ go build -o server ./monolith
```

```
$ ./server
```

```
2016/04/15 06:34:12 Starting server...
2016/04/15 06:34:12 HTTP service listening on 0.0.0.0:5000
2016/04/15 06:34:12 Health service listening on 0.0.0.0:5001
2016/04/15 06:34:12 Started successfully.
```

### Test with cURL

```
$ curl --cacert ./ca.pem -u user https://127.0.0.1:5000/login
```
```
Enter host password for user 'user':
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InVzZXJAZXhhbXBsZS5jb20iLCJleHAiOjE0NjA5ODcxOTcsImlhdCI6MTQ2MDcyNzk5NywiaXNzIjoiYXV0aC5zZXJ2aWNlIiwic3ViIjoidXNlciJ9.x3oFhRhWk5CGYfGcrNctPGWCENEsXpUuKPDQU2ZOLCY
```

> type "password" at the prompt

```
curl --cacert ./ca.pem -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InVzZXJAZXhhbXBsZS5jb20iLCJleHAiOjE0NjA5ODcxOTcsImlhdCI6MTQ2MDcyNzk5NywiaXNzIjoiYXV0aC5zZXJ2aWNlIiwic3ViIjoidXNlciJ9.x3oFhRhWk5CGYfGcrNctPGWCENEsXpUuKPDQU2ZOLCY' https://127.0.0.1:5000/
```
```
<h1>Hello</h1>
```
