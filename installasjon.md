## Raspberry pi setup

### - Installing Ubuntu
```
1. Insert mini sd card into your laptop
2. Open "Raspberry pi imager" or download from this link if not already installed: https://www.raspberrypi.com/software/
    and download it for your operative system on your laptop.
> In raspberry pi imager, select your raspberry pi model, and the mini sd card as your storage device
>> For OS click on "Choose OS" > "Other general-purpose OS" > "Ubuntu" > then choose the newest version/version on top.
```
![alt text](https://github.com/PolishCowPog/Coop_repo/blob/main/Raspberry_pi_imager.png)
```
3. click on "next" > "yes" > then wait for it to be done with writing and verifying.
4. Afterwards click on "Continue" and take out the mini sd card and insert it into your raspberry pi.
5. Turn on your raspberry pi and wait for it to turn on. a system configuration window will pop up automatically.
6. In systen configuration > Choose your language > Keyboard language > Connect to your wifi > Click on your location.
    Fill in your name, computers name, username, password and confirm password
7. Wait for ubuntu to configure.
```

### - Installing ssh
```
1. Open Terminal
2. Type "sudo apt install openssh-server"
3. Type "sudo systemctl enable ssh"
4. Type "sudo systemctl start ssh"
```

### - Sending files


### - Opening ports / firewall
```
1. type "sudo apt install ufw"
2. type "sudo ufw enable"
3. type "sudo ufw allow ssh"
```

### - Installing mariadb
```
1. Open Terminal.
2. Type "sudo apt install mariadb"
3. Type "sudo mariadb" (This will open mariadb in terminal)
4. Type "CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';"
5. Type "GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost' IDENTIFIED BY 'password';"
6. Type "FLUSH PRIVILEGES;"
```
#### Mariadb database setup
```
1. Exit mariadb by typing "exit;". you will return back to terminal
2. in terminal logg in with the new user by typing "sudo mariadb -u username -p"
3. type in the password you made
4. type "CREATE DATABASE name"
5. type "USE name;" to change into the database you just made, or use "SHOW DATABASES;" to check what databases exists.
```
