
```shell
# 将容器复制下来
sudo docker cp confluence:/opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-extras-decoder-v2-3.4.1.jar ./atlassian-extras-2.4.jar

# 复制到容器里
sudo docker cp ./atlassian-extras-2.4.jar confluence:/opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-extras-decoder-v2-3.4.1.jar.yuchuan

# confluence 授权
java -jar ./atlassian-agent.jar -m dqzboy@xxxx -n dqzboy.com -p  conf -o http://47.94.141.227:8091/ -s BR2A-OKF0-3BG0-NIDS

# confluence 插件授权
java -jar ./atlassian-agent.jar -m dqzboy@xxxx -n dqzboy.com -p com.gliffy.integration.confluence -o http://47.94.141.227:8091 -s BR2A-OKF0-3BG0-NIDS

# 新建数据库
CREATE DATABASE confluence CHARACTER SET utf8 COLLATE utf8_bin;

# 赋予用户权限
GRANT ALL PRIVILEGES ON confluence.* TO 'confluence'@'%' IDENTIFIED BY 'confluence';

flush privileges;
```
