A sonata try
===========================

仅仅只是在sonata基础上加了个前端firewall配置，方便以后私活项目直接拿来用


1.创建个数据库先

```sql
  CREATE DATABASE `symfony_sonata_dev` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
```

```bash
  app/console doctrine:schema:create
```


2.创建用户数据

*批量创建 `app/console doctrine:fixtures:load`
*手动创建 
        `app/console fos:user:create username emai@example.com password`
        `app/console fos:user:promote username ROLE_SONATA_ADMIN`


>比如我创建个用户名为zjsxwc密码为heiheihei的admin账号：

>app/console fos:user:create zjsxwc zjsxwc@126.com heiheihei

>app/console fos:user:promote zjsxwc ROLE_SONATA_ADMIN



3.创建软链

app/console assets:install --symlink --relative web






