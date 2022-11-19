## Protect your Linux Server From Hacker

### Please don't copy none commands before the ends of this article , please Don't be a script kiddie OK ?


If you use Linux and you are you are your own website in local and than you want to push it online , the first thing to do is a protect this.

When you search in your search around in  your browser 'how to secure linux server from hackers' or 'what are a best practices for protect my server' you can obtain like answers:

+ `use firewall`

  or

+ `don't use ssh with password`  a modify this file (/etc/ssh/sshd_config) and change
section **PasswordAuthentification yes** by **PasswordAuthentification no**

  or also

+ `do not use the root user`  because it's dangerous , and than the previous reason (it's not advisable to ssh into your server as superuser ,you should disable ssh as root user on the server and after create others user with sudo powers with which you can ssh into the server and if it's needed you can already switch user to root).

If you are follow well you have already understood why (because the hacker can to log in on your server and use the root power).

+ `change the default ports` because if you change the defaults ports of some services (that are more likely to be targeted like SSH & FTP), SSH is used to access the remote server and FTP is a file transfer protocol used to transfer files to and from the remote server .

If you want to change ssh port follow this:
By default ssh accepts connections through port 22 .

  `sudo nano /etc/ssh/sshd_config` 

   and search a port section and change the default number

   restart sshd service with:

`sudo systemctl restart sshd`

      **Or**

`sudo service ssh restart`
   
 `Port 2341` By example , save this file with `Ctrl + s` and exit with `Ctrl + x`
   For the port number used don't forget than port numbers 0-1023 are reserved for various system services.

For more information you can read this article on [cyberciti.biz](https://www.cyberciti.biz/faq/howto-change-ssh-port-on-linux-or-unix-server/) .


The Big problem here are than the supposedly **Best practices**  are usually unquestionned
It's for you a simple details but no , it's a one of the most important skills in **hacking**

### The Skills should not be a guesses

According you what that justify that this answers are just ? When nobody don't explain the reasoning behind something especially in IT security it's a problem ,because :

- you don't have know if this command can create anything in your computer .


## Let's go to know how to secure your Linux Server For True


SSH is used to access a linux (in our case) server remotely .

Ex: `ssh root@139.177.180.76`

A standart is `ssh user@yourserip` or others .
