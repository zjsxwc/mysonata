A sonata try
===========================

仅仅只是在sonata基础上加了个前端firewall配置，方便以后私活项目直接拿来用

创建个数据库先
CREATE DATABASE `symfony_sonata_dev` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;

app/console doctrine:schema:create

创建数据

Create the users

You can either create a handful of users like this (one of the usernames is 'superadmin' with password 'test')

./app/console doctrine:fixtures:load

Or you can manually create a user yourself

./app/console fos:user:create username emai@example.com password


./app/console fos:user:promote username ROLE_SONATA_ADMIN



比如我创建个用户名为zjsxwc密码为heiheihei的admin账号：
app/console fos:user:create zjsxwc zjsxwc@126.com heiheihei


app/console fos:user:promote zjsxwc ROLE_SONATA_ADMIN



创建软链
app/console assets:install --symlink --relative web



