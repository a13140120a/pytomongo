1. [安裝docker跟docker-compose](https://github.com/a13140120a/docker)
2. 進到yml檔在的地方輸入:`docker compose up -d`，並等待容器建好
3. 進入 mongodb 的 container(command:`docker exec -it mongodb bash`)，輸入:`db.createUser({user: "user", pwd: "user", roles:["dbOwner"]})`建立一個新的 user 要給 adminmongo 連線使用
4. adminmongo 連線輸入 `mongodb://user:1234@192.168.37.129:27017/Topic_104`(ip 視情況而定，mongodb 沒有 create db 當insert 不存在的db時會自動建立)。
