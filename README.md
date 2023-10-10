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

Then also proceeded to my web browser to run the url "http://localhost:80" to check if I could access my nginx server on the internet via my web browser

![Screenshot 2023-10-07 172427](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/4c6cb1fe-f889-4ef0-aaee-8c732bbbba01)

![Screenshot 2023-10-07 172556](https://github.com/FemiDare/phemmy_lemp_stack_project/assets/140294606/065ab18c-284c-4b5d-b3a2-ef3700366f6d)

