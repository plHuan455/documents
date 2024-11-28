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

