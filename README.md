# download_limiter
Limit download on your Ubuntu device
In order for the function to work you should have ifb module enabled and iproute installed on your Ubuntu device.

## iproute installation
To install iproute on Ubuntu run following commands:
```bash
sudo apt-get update -y
sudo apt-get install -y iproute
```
# Run script commands
To be able to run script commands you should be a root:
```bash
sudo -i 
```
Then go to folder where the script is located and type:
```bash
source ./htb_upload.sh
```
There are two commands available, one for configuring settings for ingress traffic:
```bash
set_download -d DEST_ADDRESS/MASK -s SOURCE_ADDRESS/MASK -p DEST_PORT -o SRC_PORT -l PACKET_LOSS[%] -m DELAY[ms] -r RATE[mbit or kbit]
```
To remove all rules run:
```bash
remove_download
```
