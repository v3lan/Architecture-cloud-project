bash
sudo adduser appadmin
sudo usermod -aG sudo appadmin
ini
PasswordAuthentication no
PermitRootLogin no
PubkeyAuthentication yes
bash
sudo systemctl restart sshd
bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw enable
bash
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 
-keyout /etc/ssl/private/nginx-selfsigned.key 
-out /etc/ssl/certs/nginx-selfsigned.crt
bash
sudo nginx -t
sudo systemctl reload nginx
