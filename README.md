# 整合nginx jenkins agent 
### 使用nginx 作為https proxy

# 使用方式
- docker-compose build
- create ssl 憑證
```
test ! -d ./data/nginx/ssl && mkdir -p ./data/nginx/ssl
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./data/nginx/ssl/server.key -out ./data/nginx/ssl/server.crt
``` 
- docker-compose up -d
- 建立agent,取得secret
- 修改docker-compose ，並重啟
