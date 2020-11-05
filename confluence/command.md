
```shell
# 将容器复制下来
sudo docker cp confluence:/opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-extras-decoder-v2-3.4.1.jar ./atlassian-extras-2.4.jar

# 复制到容器里
sudo docker cp ./atlassian-extras-2.4.jar confluence:/opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-extras-decoder-v2-3.4.1.jar.yuchuan

# 新建数据库
CREATE DATABASE confluence CHARACTER SET utf8 COLLATE utf8_bin;

# 赋予用户权限
GRANT ALL PRIVILEGES ON confluence.* TO 'confluence'@'%' IDENTIFIED BY 'confluence';

flush privileges;
```
