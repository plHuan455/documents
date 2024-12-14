# NGINX

## SSL
- Step 1: Install libs
```bash
sudo apt install certbot python3-certbot-nginx
```

- Verify web server ports are open and allowed through Firewall
```bash
sudo ufw status verbose
```

- Step 2: Obtain and SSL certificate
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

- Step 3: add config nginx
```nginx
# { ...
    listen 443 ssl;
    server_name domain.com;

    ssl_certificate /etc/letsencrypt/live/stg-api.tonfarms.com/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/stg-api.tonfarms.com/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf;
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem;
# ... }
```


> **_NOTE:_**  <a href="https://www.youtube.com/watch?v=t35Mmyxmgto&lc=UgxlO2h5x4qYmyW1QW14AaABAg.AAUidaxuxA9AAUskHVlCun">Link</a>

