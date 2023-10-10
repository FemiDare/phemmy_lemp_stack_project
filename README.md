# phemmy_lemp_stack_project

First off, I launched an EC2 instance named "my_ubuntu_space" on my AWS account and connected to said instance via my git bash terminal.

I then ran a "sudo apt update" command to update my OS.

![Screenshot 2023-10-07 170214](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/6b69e5e5-828b-4361-9ef4-ddd0d8091420)

![Screenshot 2023-10-07 170838](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/2a3034ff-eb0b-472c-a964-b60d0cfc9199)

![Screenshot 2023-10-07 170933](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/f486750d-9ea9-4155-b353-e7d5084e1a22)

![Screenshot 2023-10-07 171023](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/ab16cd9a-a320-4cde-b9f6-bd776b1a1060)

![Screenshot 2023-10-07 171124](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/bec31d33-926b-4cae-a73a-d45fd5ad292c)

I then proceeded to install nginx using the command "sudo apt install nginx -y".

On completion of the installation of nginx. I ran the command "sudo systemctl status nginx", so as to accertain that nginx was installed properly and active on my system

![Screenshot 2023-10-07 171257](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/976f3169-50cc-461d-89a1-a730a20f6bf9)

![Screenshot 2023-10-07 171354](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/3c21ad89-5dc0-4f66-a33e-4651d7b8e16e)

I was then supposed to go to my security group and open TCP port 80 so as to allow traffic to the server as web browsers listen on that port

but I had previously opened the port at the initial setup of my security group when I was launching the instance so I just did a double check to ensure that TCP port 80 was open

![Screenshot 2023-10-07 171653](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/857657dd-d92e-4fb5-9a7b-3e09d0fe315d)

Then using the "curl http://localhost:80" command I checked if I could access nginx server from my ubuntu shell

Then also proceeded to my web browser to run the url "http://<my-public-ip-address>:80" to check if I could access my nginx server on the internet via my web browser

![Screenshot 2023-10-07 172427](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/4c6cb1fe-f889-4ef0-aaee-8c732bbbba01)

![Screenshot 2023-10-07 172556](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/065ab18c-284c-4b5d-b3a2-ef3700366f6d)

I then proceeded to install mysql on my machine using the command "sudo apt install mysql-server"

You will observe that I had some issues getting the mysql server installed initially and had to try to see what the issue was by checking if it was previously installed and checking the commands before getting it done.

I then checked to verify that mysql was properlly installed by running the command "sudo mysql" to gain access and exiting mysql after confirmation on successful installation

![Screenshot 2023-10-07 173547](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/3c28161a-44ed-4e93-87fa-f018a24a1869)

![Screenshot 2023-10-07 173956](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/ef4a3e08-eb7d-4301-a18d-d67cb9c7945e)

I then proceeded to further secure mysql server by assigning a password and configuring the security measures i.e security password strenght and user access

![Screenshot 2023-10-07 174149](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/12357bb0-06b6-4095-bc6a-9661d2c8e879)

![Screenshot 2023-10-07 174508](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/4a9a49a0-94e8-4024-91cd-28b6a4e64b7b)

![Screenshot 2023-10-07 174555](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/8ef9adb1-54c9-4a55-9876-10b6faa5b769)

Next I proceeded to installing php on my ubuntu machine

![Screenshot 2023-10-07 180611](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/667867c2-1174-41a0-b89e-07bb6b9fa8f8)

Then I created a root web directory/folder using the command "sudo mkdir /var/www/myprojectLEMP and assigned ownership of the directory using $USER

I then opened a new configuration file "myprojectLEMP" under the nginx sub-directory "sites-available" using the "nano" editor

I had a problem saving the codes I had scripted into the file being I was getting a permission denied error. So I had to exit without saving and create and edit the file using the sudo command

![Screenshot 2023-10-07 181412](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/b20263c0-a3df-41a8-8c71-a7beb18641cf)

![Screenshot 2023-10-07 182105](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/fea7a20c-c53f-41e6-8e37-6220fddda6c7)

![Screenshot 2023-10-07 182209](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/f02d7d32-ba35-4dd4-8ec1-0168152a13e4)

Then I had to activate my configuration by going to the nginx's sub-directory "sites-enabled" and linking the config file and then testing for syntax errors by running the command "sudo nginx -t"

I encountered some issues being I had linked a file with the wrong name and had to do some manuevering to correct the mistake before getting a successful result from running the command "sudo nginx -t" 

After that I unlinked the default site file and reloaded nginx using the command "sudo systemctl reload nginx"

![Screenshot 2023-10-07 183044](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/83be0849-543f-4f8d-b356-9baf8381c37f)

Next we create a new landing page by echoing into a new index.html in our web directory and test it using our public ip address and and DNS name on the web browser 

![Screenshot 2023-10-07 183153](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/83192442-d82b-486c-ad7b-024addd29fad)

![Screenshot 2023-10-07 183222](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/a52a0f00-450f-4d89-aa9e-faf4e935eb82)

![Screenshot 2023-10-07 183430](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/4dfc60ff-4b56-4c7f-862d-ec22d2218ec2)

I then created a test php file in my directory root named "info.php" pasted an info code in the file and tested it on my web browser

![Screenshot 2023-10-07 183603](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/46a6920b-2594-47b5-8d05-6574c2e28de0)

![Screenshot 2023-10-07 183733](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/33298725-723c-4002-9f56-15823113cb77)

Thereafter I proceeded to attempt creating a database in mysql 

![Screenshot 2023-10-07 185027](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/d9ec51d6-87a2-40b0-af90-0cf2fef1a1fd)

![Screenshot 2023-10-07 190144](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/38c693a1-1df8-4867-b1bb-83623ff11511)

![Screenshot 2023-10-07 193350](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/8e3ea7bc-e233-4d1d-82f8-96053199ad17)
