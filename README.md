# test_plate  
基于Django的轻量级接口测试平台  



***



***
# 设计思想  
1、 模拟性能测试工具JMeter的思路，实现接口测试与性能测试的Web化；  
2、 计划有产品模块、接口测试用例模块、性能测试用例模块、任务队列模块、测试报告模块等；  
3、 前期采用Django+Bootstrap前后端不分离的模式实现功能，后期再严格按照RESTful的风格来编程。  


***
# 本地调试  
`python manage.py collectstatic`  
复制xadmin静态文件  

`python manage.py makemigrations`  
激活模型  

`python manage.py migrate`  
迁移  

`python manage.py createsuperuser`  


`python manage.py runserver`  
启动服务 

后台  
http://127.0.0.1:8000/admin/


***
# 本地打包  
`docker build -t dapi .`  
dapi为镜像名称，随便取  

`docker run -d --name dapi2020 -p 80:80 mock:latest`  
启动容器  
后台运行  
给容器取个别名dapi2020  
映射80端口  

后台  
http://x.x.x.x/admin/  
宿主机的IP地址  
账号：admin  
密码：test123456  

前台  
http://x.x.x.x/  
宿主机的IP地址  
账号：admin  
密码：test123456

`docker exec -it dapi2020 /bin/bash`  
进入容器内部

`exit`  
退出容器内部

`docker stop dapi2020`  
停止容器  

`docker rm dapi2020`  
删除容器  
