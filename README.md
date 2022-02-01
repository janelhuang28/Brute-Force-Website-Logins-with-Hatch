# Brute-Force-Website-Logins-with-Hatch
Brute forcing website logins with Hatch

## Prerequisites

1. Download Selenium with ``pip2 install selenium`` (If pip not used install with ``sudo apt-get install python-pip``)
2. Download Requests with ``pip2 install requests``
3. Install chrome driver from https://chromedriver.chromium.org/downloads (with the appropriate chrome driver version)
4. Unzip the driver and move to ``/usr/bin`` 
5. Download Hatch with ``git clone https://github.com/nsgodshall/Hatch.git`` 
6. Add the following line to main.py ``driver = webdriver.Chrome('/usr/bin/chromedriver', chrome_options=chrome_opt>``

## Scan for Targets

To see the open targets use ``sudo nmap -p 80,8080,81,8081,443 <iprange>`` (the IP range can be found by running ipcalc``
 The result should be like so: ![image](https://user-images.githubusercontent.com/39514108/151937255-c6e3296a-5eb8-43bb-b51b-b22c8742d520.png)
Select the website with the open port. Use the address bar and type ``<IP>:<Port>``
  
## Run Hatch 
1. To run hatch execute ``python2 main.py``
2. Enter the website from before
3. Admin, password and login button should be found by inspecting the element with (Copy Selector). Example: #adminPassword
4. Use custom or default ``passlist.txt`` as the password list.
  
Now the process should begin to automate.
  
  ![image](https://user-images.githubusercontent.com/39514108/151937651-b824482b-adbf-48d0-ba6e-f1d8223dc901.png)
If the password is found it should output the following:
  
  ![image](https://user-images.githubusercontent.com/39514108/151939717-b276b125-cfac-48bf-b529-51024fb6bbb0.png)
