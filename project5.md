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



