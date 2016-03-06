# Minecraft-Server-autostart-script
Minecraft init.d script to automatic start minecraft server on boot as diferent user.

(If creating more server change minecraft1 to minecraft2 /see file minecraft2)

![Build Status](https://img.shields.io/badge/Build Status-passed-green.svg)
![Minecraft](https://img.shields.io/badge/tested%20minecraft-craftbukkit%201.9-yellow.svg)
![java](https://img.shields.io/badge/java-version%201.8.0__66-orange.svg)
![os](https://img.shields.io/badge/tested OS-Ubuntu server 15.10 x64-blue.svg)
##Requirements
- debian based OS
- sudoers   (```aptitude install sudo```)
- nano editor (```sudo apt-get install nano```)
- screen (```sudo apt-get install screen```)
- downloaded minecraft/craftbukkit/spigotmc/bungeecord
- dir location of mc /opt/minecraft1/
- installed java version 8 (```sudo apt-get install oracle-java8-installer```)
- user minecraft  (```sudo adduser --disabled-login minecraft```) 
- permission for minecraft user (```sudo chown minecraft:minecraft -R /opt/minecraft1```)


##How to build
1. Terminal/Console:

    ``` sh
     cd /etc/init.d
    ```
    ``` sh
     nano minecraft1
    ```

2. paste/rewrite code from minecraft1 file [minecraft1](https://github.com/Yamiru/Minecraft-Server-autostart-script/blob/master/minecraft1) 
3. CTRL+X
4. Y
(name:minecraft1)
5. ENTER 
6. Terminal/Console:


    ```
     sudo chmod 755 /etc/init.d/minecraft1
    ```
7. Terminal/Console:

    ```
     sudo update-rc.d minecraft1 defaults
    ```


8. Terminal/Console:

``` reboot ```


 
##Commands

stop  Minecraft1 Server :  ```     service minecraft1 stop    ```
    
start Minecraft1 Server :  ```     service minecraft1 start    ```



Chceck java version ```     java -version    ```
If you change /etc/init.d/minecraft1 file --->  ```  sudo minecraft1 ts3server defaults ```    &   ```     systemctl daemon-reload    ```  
If not work starting try to stop ```     service minecraft1 stop    ``` 
check screen sessions ```     screen -ls    ```
show screen session minecraft1 ```     screen -x minecraft1    ```

If not work starting try to stop ```     service minecraft1 stop    ```  and start again  ```     service minecraft1 start    ```  !!!
