sudo apt install openssh-server

sudo systemctl enable --now ssh

sudo systemctl status ssh



Allow SSH connections:
bash
sudo ufw allow ssh
Enable the firewall (if it's not already enabled):
bash
sudo ufw enable
Verify the firewall status:
bash
sudo ufw status
