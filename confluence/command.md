```shell
# confluence 授权
java -jar /Users/liuyuchuan/Desktop/docker-composes/confluence/build/atlassian-agent-v1.2.3/atlassian-agent.jar -m dqzboy@xxxx -n dqzboy.com -p  conf -o http://47.94.141.227:8090/ -s BXFT-PSHE-OG2Y-RGMK

# confluence 插件授权
java -jar /Users/liuyuchuan/Desktop/docker-composes/confluence/build/atlassian-agent.jar -m dqzboy@xxxx -n dqzboy.com -o https://confluence.66plat.com/ -s B6IF-QR11-DET9-R943 -p de.actonic.inline-table-editing

# 新建数据库
CREATE DATABASE confluence CHARACTER SET utf8 COLLATE utf8_bin;

# 赋予用户权限
GRANT ALL PRIVILEGES ON confluence.* TO 'confluence'@'%' IDENTIFIED BY 'confluence';

flush privileges;
```
