```
# jira 授权
java -jar /Users/liuyuchuan/Desktop/docker-composes/confluence/build/atlassian-agent.jar -m dqzboy@xxxx -n dqzboy.com -p jira -o http://localhost:8080/ -s BCPD-0F0Q-5GLE-8UCG

# 新建数据库
CREATE DATABASE jira CHARACTER SET utf8mb4 COLLATE utf8mb4_bin;

# 赋予用户权限
create user 'jira'@'%' identified by 'jira';
GRANT ALL PRIVILEGES ON jira.* TO 'jira'@'%';

flush privileges;
```
