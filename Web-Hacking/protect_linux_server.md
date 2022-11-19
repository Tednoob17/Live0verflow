## Protect your Linux Server From Hacker

If you use Linux and you are you are your own website in local and than you want to push it online , the first thing to do is a protect this.

When you search in your search around in  your browser 'how to secure linux server from hackers' or 'what are a best practices for protect my server' you can obtain like answers:


+ `use firewall`

  or

+ `don't use ssh with password`  a modify this file (/etc/ssh/sshd_config) and change
section **PasswordAuthentification yes** by **PasswordAuthentification no**

  or also

+ `do not use the root user`  because it's dangerous , and than the previous reason (it's not advisable to ssh into your server as superuser ,you should disable ssh as root user on the server and after create others user with sudo powers with which you can ssh into the server and if it's needed you can already switch user to root)

If you are follow well you have already understood why (because the hacker can to log in on your server and use the root power)
