# Docker-on-AWS-EC2-Instance
Docker Installation on AWS EC2 Instance. This is to show how to install Docker on an AWS EC2 instance. We'll walk you through setting up Docker  on your Amazon EC2 server. 


### Launch Amazon EC2

<img width="1020" alt="Screen Shot 2024-01-30 at 7 46 47 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/d36f739e-f040-40bc-a655-74f91dfd13f2">

<img width="975" alt="Screen Shot 2024-01-30 at 7 47 08 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/a5c96dc8-9576-497b-b4c3-17b40dc6c8b6">

### Connect to instance 

<img width="1201" alt="Screen Shot 2024-01-30 at 7 48 41 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/020926e5-a225-4d15-8363-a36f4e53bc90">

### To Update the instance 

```
  sudo yum update -y

```

### Install Docker
```
sudo yum install docker -y
```
<img width="1236" alt="Screen Shot 2024-01-30 at 8 03 30 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/cd529b86-b023-4e26-8b3a-4f85724fe262">


### Start Docker 
```
sudo service docker start
```
<img width="1276" alt="Screen Shot 2024-01-30 at 8 05 05 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/253e4ea5-7985-4c97-a992-051e0ff2fe28">


### Check the service 
```
sudo service docker status
```
<img width="1237" alt="Screen Shot 2024-01-30 at 8 06 46 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/396a7926-25a6-486d-b4b4-8c9c45cb3f86">



### Check the Docker version
```
sudo docker version
```
<img width="1226" alt="Screen Shot 2024-01-30 at 8 10 16 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/44fec7c5-0451-409a-b2f4-3006b5cf2d6b">


### Let's search and pull the nginx image
```
sudo docker search nginx
sudo docker pull nginx
```
<img width="1231" alt="Screen Shot 2024-01-30 at 8 14 30 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/59ba5579-28ba-49a1-adcb-a10420a30a54">


### Check for the images on the docker
```
sudo docker images
```
<img width="1226" alt="Screen Shot 2024-01-30 at 8 15 37 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/5489fa16-9959-4375-b51f-fc745f62f658">


### Let's create a container with the nginx image
```
sudo docker run -d -p 80:80 nginx
sudo docker ps
```
<img width="1232" alt="Screen Shot 2024-01-30 at 8 20 02 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/47e0fb90-3fb8-47c6-baed-36e908858725">


### Use the EC2 instance public IP to check for the Nginx welcome page
<img width="1258" alt="Screen Shot 2024-01-30 at 8 21 45 PM" src="https://github.com/gakas14/Docker-on-AWS-EC2-Instance/assets/74584964/272684e0-6bc0-4166-bbbd-34d87a2e3038">

### to stop a container
```
sudo docker stop <id>
```
### to remove the image
```
sudo docker rmi <image_name/image_id>
```


