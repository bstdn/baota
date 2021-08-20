# BAOTA (宝塔)

- 一键运行**宝塔**

## 快速使用

1. `clone`项目

    ```
    git clone https://github.com/bstdn/baota.git
    ```

2. 如果不是`root`用户，还需将当前用户加入`docker`用户组

    ```
    sudo gpasswd -a ${USER} docker
    ```

3. 拷贝并命名配置文件（Windows系统请用copy命令）

    ```
    $ cd baota                                          # 进入项目目录
    $ cp env.sample .env                                # 复制环境变量文件
    $ cp docker-compose.sample.yml docker-compose.yml   # 复制 docker-compose 配置文件
    $ docker-compose up -d                              # 后台运行
    ```

4. 在浏览器中访问：`http://127.0.0.1:8888`或`http://localhost:8888`

5. 使用`docker exec -it bt bash`进入到宝塔容器

6. 在容器中输入命令`bt`回车，使用`宝塔面板命令行`可进行账号密码初始化

7. 关闭安全出口

    ```
    rm -f /www/server/panel/data/admin_path.pl
    ```
