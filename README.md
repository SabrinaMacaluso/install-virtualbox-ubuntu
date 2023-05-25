# Installing VirtualBox6.1 on Ubuntu20.04


```bash
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
echo "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian focal contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list
sudo apt update
sudo apt install virtualbox-6.1
vboxmanage --version
```
  

## How to uninstall VirtualBox

```bash
sudo apt-get purge Virtualbox*
rm -rf ~/.config/VirtualBox
```

## Using the Scripts

```bash
chmod +x install_virtualbox.sh
chmod +x uninstall_virtualbox.sh
```
To install VirtualBox, run ```./install_virtualbox.sh```
To uninstall VirtualBox, run ```./uninstall_virtualbox.sh```


## Troubleshooting

If the first command keeps loading, you can try the following steps:

1. Copy the link into your browser: [https://www.virtualbox.org/download/oracle_vbox_2016.asc](https://www.virtualbox.org/download/oracle_vbox_2016.asc).

2. Copy the contents of the webpage and save them as `oracle_vbox_2016.asc` file.

3. Open a terminal and navigate to the directory where you saved the file.

4. Run the following command:

   ```bash
   sudo apt-key add oracle_vbox_2016.asc
