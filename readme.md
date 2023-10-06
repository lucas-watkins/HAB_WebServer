# Setup
1. First obtain a server from Oracle's Oracle Cloud Infrastructure (OCI) free tier. Make sure the server runs on Ubuntu and uses the E2.Micro shape

2. SSH into server using openSSH to access server command line. You can use this command to do so. Don't forget your SSH private key file because that is required to authenticate with the server. 

    ```
    ssh ubuntu@ipaddr -i "path to key file"
    ```

3. Then update the server and reboot it by running these commands which run the server package manager to update the server.

    ```
    sudo apt update
    sudo apt upgrade
    sudo reboot
    ```
4. Clone this github repository onto the server by running

    ```
    git clone https://github.com/lucas-watkins/HAB_WebServer.git
    ```

5. Change directories into the web server by running

    ```
    cd HAB_WebServer
    ```

6. Install nodejs and npm
    ```
    sudo apt install nodejs
    sudo apt install npm
    ```

7. Install dependencies of the web server

    ```
    npm install express
    npm install socket.io
    npm install ftp-srv
    npm install node-nmea
    npm install express-photo-gallery
    npm install sleep
    ```

    ~~8. Write server ip address into code. Run the following line to open file~~~

    ~~sudo apt install nano
    nano server.js~~

~~Then replace "my server ip" with the public ip adress of the server. Press control + x to exit and save when it asks you to save.~~

9. Open Server Ports 8080, 8081, 8082, 8083, and 8110 by following this guide. The guide below states to open ports 80 and 443 but replace the destination ports with the ports above.

    [Open ports for OCI Servers](https://cleavr.io/cleavr-slice/opening-port-80-and-443-for-oracle-servers)
