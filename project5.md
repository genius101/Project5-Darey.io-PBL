<h1> In this project, we would be implementing a Client Server Architecture using MySQL Database Management System (DBMS)</h1>

![Client-server](https://user-images.githubusercontent.com/10243139/124310749-90f32b00-db64-11eb-9c2b-3fbcc5e18312.png)

<h2> The Project is explained as follows: </h2>

<p>In the example above, a machine that is trying to access a Web site using Web browser or simply ‘curl’ command is a client and it sends HTTP requests to a Web server (Apache, Nginx, IIS or any other) over the Internet.</p>

<p>To demonstrate a basic client-server using MySQL RDBMS, follow the below instructions:</p>

<h2>Step 1: Create and configure two Linux-based virtual servers (EC2 instances in AWS) and Install MySQL on both</h2>

<p>Update Ubuntu on both Virtual Machines:</p>

- [x] sudo apt update

<p>Install my-sql server on the first machine to act as the server:</p>

- [x] sudo apt install mysql-server

<p>Install my-sql client on the second machine to act as the client:</p>

- [x] sudo apt install mysql-client

<h2>Step 2: Update Inbound rules in Security Groups to allow TCP port 3306 for specific IP address</h2>

![2](https://user-images.githubusercontent.com/10243139/124318458-98203600-db70-11eb-9f11-60ce1a4f8736.jpg)

<h2>Step 3: Run this command to improve the security of mysql: sudo mysql_secure_installation</h2>

![3](https://user-images.githubusercontent.com/10243139/124318520-ac643300-db70-11eb-908f-23760b28124e.jpg)

<h2>Step 4: You might need to configure MySQL server to allow connections from remote hosts</h2>

<p> Edit the MYSQL Conf file:
  
- [x] sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf 

<p>Replace ‘127.0.0.1’ to ‘0.0.0.0’ on bind-address</p>
	
<p>After saving the file, run the following command to effect the configuration:</p>
	
- [x] sudo systemctl restart mysql

![4](https://user-images.githubusercontent.com/10243139/124318853-357b6a00-db71-11eb-885c-b501362635f0.jpg)

<h2>Step 5: Create a user and a database linked to the user</h2>

![5](https://user-images.githubusercontent.com/10243139/124318870-3d3b0e80-db71-11eb-9503-72b94fba2ecc.jpg)

<h2>Step 6: Log in to the server from the client and access database</h2>

![6](https://user-images.githubusercontent.com/10243139/124318915-504dde80-db71-11eb-852e-ef3e744eb9a9.jpg)


