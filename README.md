# securityonion-grr
**Install Google GRR on top of Security Onion**  
`sudo wget https://raw.githubusercontent.com/weslambert/securityonion-grr/master/install_grr`   
`sudo chmod +x install_grr`   
`sudo ./install_grr`   

**Add firewall rules**   
Analyst/Web Interface:      
`sudo so-allow`     
OR   
`sudo ufw allow proto tcp from REMOTE_IP to any port 443`   

GRR Client IP:   
`sudo iptables -I DOCKER-USER ! -i docker0 -o docker0 -s ClIENT_IP -p tcp --dport 8080 -j ACCEPT`   
