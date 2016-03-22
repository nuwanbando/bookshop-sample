# bookshop-sample
the book ordering work-flow / integration scenario with a docker based deployment

The project setups a orchestration scenario with WSO2 ESB / BPS & DSS. 

The setup deploys in dockers. 

# navigate to the docker build path
$ cd dockerfiles/bookshop

# execute the docker composer
$ docker-compose up -d

# send the following request {replace the host with docker vm ip/host}

POST /bookbag HTTP/1.1
Host: 192.168.99.100:8290
Cache-Control: no-cache
Postman-Token: c039825e-d9c1-50de-6d6f-e9356dcf3e00
Content-Type: application/x-www-form-urlencoded

customerName=nuwan&customerEmail=nuwan%40wso2.com&bookId=B20&quantity=10

DSS - offset 0
ESB - offset 10
BPS - offset 20

mysql - port 3306