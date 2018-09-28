EC2

Amazon Elastic Compute Cloud (Amazon EC2) 是一种提供可调节计算容量的 Web 服务 – 简单来说，就是 Amazon 数据中心里的服务器 – 您可以使用它来构建和托管您的软件系统。



# Amazon Elastic Container Registry (Amazon ECR) 

是一项完全托管的 Docker 容器注册表服务，可让开发人员轻松存储、管理和部署 Docker 容器映像。



# Amazon Elastic Container Service (Amazon ECS)

 是一项高度可扩展的快速容器管理服务，可轻松运行、停止和管理 Amazon EC2 实例群集上的 Docker 容器。

- to run, stop, and manage Docker containers on a cluster



# CLI

### batch 

https://docs.aws.amazon.com/zh_cn/cli/latest/reference/batch/index.html

- job submit
- cancel
- queue
- 



auto scaling

https://docs.aws.amazon.com/zh_cn/cli/latest/reference/autoscaling/index.html

https://docs.aws.amazon.com/zh_cn/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html



# IAM (Identity and Access Management)

https://aws.amazon.com/cn/iam/



# EC2

Amazon Elastic Compute Cloud (Amazon EC2) 是一种提供可调节计算容量的 Web 服务 – 简单来说，就是 Amazon 数据中心里的服务器 – 您可以使用它来构建和托管您的软件系统。



# Amazon Elastic Container Registry (Amazon ECR) 

是一项完全托管的 Docker 容器注册表服务，可让开发人员轻松存储、管理和部署 Docker 容器映像。



# Amazon Elastic Container Service (Amazon ECS)

 是一项高度可扩展的快速容器管理服务，可轻松运行、停止和管理 Amazon EC2 实例群集上的 Docker 容器。

- to run, stop, and manage Docker containers on a cluster



# CLI

### batch 

https://docs.aws.amazon.com/zh_cn/cli/latest/reference/batch/index.html

- job submit
- cancel
- queue
- 



# Auto scaling

https://docs.aws.amazon.com/zh_cn/cli/latest/reference/autoscaling/index.html

https://docs.aws.amazon.com/zh_cn/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html



# IAM (Identity and Access Management)

https://aws.amazon.com/cn/iam/





# AWS from LinuxAcademy

 * [AWS concept](https://www.youtube.com/watch?v=LKStwibxbR0&index=1&list=PLv2a_5pNAko2Jl4Ks7V428ttvy-Fj4NKU)
	 * VPC: virtual private cloud
 * [AWS Essentials](https://www.youtube.com/watch?v=BDBvHOaaKHo&list=PLv2a_5pNAko0Mijc6mnv04xeOut443Wnk)
 * [Google Cloud Platform (GCP) for AWS user](https://www.youtube.com/watch?v=IotvQOfdPnA&list=PLv2a_5pNAko1E-W-vjl9SSzDyOljP0-AX)
 * [Project Omega Interactive guide link](http://bit.ly/2guw5gY)




### S3 
* S3 class
	* standard
	* Reduced Redundancy Storage
	* S3-IA
	* Glacier (Archive
* create life-cycle role
* permissions； public sharing
* Versioning


### IAM: Identity and access management
user and group: police and roles
* roles (allow instant (EC2) to access other service (S3) )

### VPC
* Internet GateWay (IGW): like a 路由器
* Route table: provide IP
* NACLs (Network access control lists) ： like a firewall
* subnet <-> Route table
	* public can access internet
	* private can NOT access internet

### RDS w
ith DynamoDB
* RDS:
	* MySQL; Microsoft SQL; PostgreSQL 
* resizeable capacity

* SSH tunning

### SNS 
* simple notification service
	* publishers
	* subscribers

### HPC
https://aws.amazon.com/cn/hpc/?nc1=f_dr

