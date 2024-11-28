# NGINX

## SSL
- Install libs
```bash
sudo apt install certbot python3-certbot-nginx
```

- Verify web server ports are open and allowed through Firewall
```bash
sudo ufw status verbose
```

- Obtain and SSL certificate
```bash
sudo certbot --nginx -d  your_domani.con -d ...
```

- Check status of certbot
```bash
sudo systemctl status certbot.timer
```

- Check list domain have ssh
```bash
ls /etc/letsencrypt/live
```



> **_NOTE:_**  <a href="https://www.youtube.com/watch?v=t35Mmyxmgto&lc=UgxlO2h5x4qYmyW1QW14AaABAg.AAUidaxuxA9AAUskHVlCun">Link</a>

