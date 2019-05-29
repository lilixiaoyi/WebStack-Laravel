# WebStack-Laravel

一个开源的网址导航网站项目，具备完整的前后台，您可以拿来制作自己的网址导航。

![首页](public/screen/01.png)



## 部署

克隆代码：

```shell
git clone https://github.com/hui-ho/WebStack-Laravel.git
```

该项目基于php运行，因此需要配置php基础环境，可以使用Apache+PHP+MySQL。

此外需要安装composer，下面语句会下载一个composer文件
```shell
curl -sS https://getcomposer.org/installer | php
```

安装依赖：

```shell
$ composer install
```
如果上面无法执行，建议使用下面命令替代：
```shell
php composer.phar install
```

编辑配置：

```
$ cp .env.example .env
```

新建一个mysql的数据库
```shell
CREATE SCHEMA `homenav` DEFAULT CHARACTER SET utf8mb4 ;
```
...
DB_DATABASE=database
DB_USERNAME=username
DB_PASSWORD=password
...
```

生成 KEY：

```shell
$ php artisan key:generate  
```

迁移数据：

```shell
php artisan migrate:refresh --seed
```

开启服务：

```shell
$ php artisan serve
```

安装完成：http://127.0.0.1:8000



## 使用

后台地址：http://domain/admin

默认用户：admin

默认密码：admin

![主页](public/screen/02.png)

![分类](public/screen/03.png)

![网站](public/screen/04.png)



## 感谢

前端设计：[**WebStackPage**](https://github.com/WebStackPage/WebStackPage.github.io)

后台框架：[**laravel-admin**](https://github.com/z-song/laravel-admin)



## License

MIT
