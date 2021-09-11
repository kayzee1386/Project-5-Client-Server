# Project-5-CLIENT-SERVER ARCHITECTURE WITH MYSQL

This project showcase how Client-Server is an architecture as it details how two or more computers are connected together over a network to send and receive requests between one another. The one sending request is regarded as the `Client` while that responding is called `Server`.

Below shows a simple client-server communication with the use of below command;
`curl -Iv www.propitixhomes.com`

![curl](https://user-images.githubusercontent.com/46185705/132881004-b42d0cd6-9a57-4274-a46f-0927e0e8a023.jpg)

![curl-2](https://user-images.githubusercontent.com/46185705/132882560-406122a0-f072-4df0-b2ff-c32c91081912.jpg)

### Step 1: 

Two ubuntu instances were launched and named `mysql-server` and `mysql-client` respectively.

![client-server](https://user-images.githubusercontent.com/46185705/132883003-bd23859e-9839-4ca3-83c6-7830f0c54ac8.jpg)

### Step 2 and 3:

This stage involves the installations of mysql on both instances and the following were carried out majorly on the server-side but i'll always indicate where the same command were ran for the two;

`sudo apt update` were ran on both instances;

![sudo-apt](https://user-images.githubusercontent.com/46185705/132884682-7663b9e5-c6fe-439a-833a-e378461412bb.jpg)
![sudo-apt-client](https://user-images.githubusercontent.com/46185705/132885003-04e7cc62-53d4-4667-a07e-1daffe9291df.jpg)

`sudo apt install mysql-server -y` for the server side and
`sudo apt install mysql-client -y` for the client-side as well

![mysql-server-installed](https://user-images.githubusercontent.com/46185705/132886613-53741129-77b3-4424-802a-e7b49dbea533.jpg)

`sudo mysql_secure_installation` was ran only on the server side and below is the output
![mysql-server-secured](https://user-images.githubusercontent.com/46185705/132886837-4f9adc99-5775-4fdf-a861-388e976eca98.jpg)

Also, `sudo systemctl enable mysql` command was used to enable the server
![mysql-enabled](https://user-images.githubusercontent.com/46185705/132887176-a858f81e-63b3-4b64-b0ba-7f817a595d1a.jpg)

### Step 4:

The Mysql port of 3306 was enabled in the mysql-server instance which is to allow mysql-client to access the database of the server. Also, only the mysql-client's IP were allowed for security purposes.

![tcp-3306](https://user-images.githubusercontent.com/46185705/132939197-88a95ca9-2576-4006-9d36-0e70f33b4571.jpg)

On the mysql-server instance, some configuration were carried out on the mysql server, see output result below;

![logon-mysql-server-db](https://user-images.githubusercontent.com/46185705/132939391-895ce78b-2540-46cc-b8c0-4ddc784d4999.jpg)

![remote-user](https://user-images.githubusercontent.com/46185705/132939439-b27741ba-b61a-4d5b-aaaa-2cda42c50b69.jpg)

![mysql-enabled](https://user-images.githubusercontent.com/46185705/132943805-57f6963d-13de-4605-8c6b-4afcf3a49330.jpg)

![mysql-server-secured](https://user-images.githubusercontent.com/46185705/132939434-4f4671d7-f5f8-48ef-ba7b-b278815128fd.jpg)


### Step 5, 6 & 7:

In other to allow the mysql-client to be able to access mysql-server this command was ran `sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf` and where we've this 
IP address `127.0.0.1` replaced with `0.0.0.0` respectively.

`ip address show` command was used to display the IP address of the server which was used to access the mysql of the server from the client's terminal

![IP-address](https://user-images.githubusercontent.com/46185705/132944032-b52b42d7-923b-45e7-9279-bb6a6551c843.jpg)

`sudo systemctl restart mysql` was used to restart the mysql-server before launching it at the client's side

And finally, the server was launched from the mysql-client using this command `sudo mysql -u remote_user -h (public IP of the mysql-server) -p` while inside the database, 
`show databases` command was ran and below was the final output.

![Final-update](https://user-images.githubusercontent.com/46185705/132948142-29c4b819-c69f-47eb-8338-5e2a4f0d4a12.jpg)

```
                                                
                                                Thanks and God Bless! ✌
                                                
```

























