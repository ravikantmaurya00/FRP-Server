# FRPS-Server
## Step to run FRP Server in AWS EC2 Instance
- Step 1: Log in to your AWS Account and open EC2 Instance .
- Step 2: Then Launch  Instance .
  
  ![]( https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/1.png)
  ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/2.png)
  ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/3.png)
  ![Launced Instance](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/4.png)
- Step 3: After launching select the Instance and click on ***Connect***.
  ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/5.png)
- Step 4: After this update  your system.
     ```
     sudo su
     sudo apt update
     sudo apt upgrade -y
     ```
     ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/6.png)
     ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/7.png)
- Step 5: Download FRP Server.
  
   ```wget https://github.com/fatedier/frp/releases/download/v0.47.0/frp_0.47.0_linux_amd64.tar.gz```
  ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/8.png)
- Step 6: Extract the downloaded ***tar.gz file*** .
  
     ```tar -xvzf frp_0.47.0_linux_amd64.tar.gz```
- Step 7: Move to the FRP Folder.
  
     ```cd frp_0.47.0_linux_amd64```
- Step 8: Edit the ***frps.ini file *** with nano or your preferred text editor.
  
     ```nano frps.ini```
- Step 9: Example  of Configuration for frps.ini:
     ```
   [common]
  bind_port = 7000
  vhost_http_port = 80
  vhost_https_port = 443
  dashboard_port = 7500
  dashboard_user = admin
  dashboard_pwd = admin
     ```
- Step 10: Run the FRP Server.
  
   ```./frps -c ./frps.ini```
  ![](https://github.com/ravikantmaurya00/FRPS-Server/blob/main/ScreenShot/9.png)
  
    
