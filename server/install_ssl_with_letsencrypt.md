1. Installing Certbot
```
sudo apt install certbot python3-certbot-apache
```

2. Check apache virtual host
```
sudo nano /etc/apache2/sites-available/your_domain.conf (If you have ServerName & ServerAlias there close the editor and go to next step)
```

3. Test your apachectl configaration
```
sudo apache2ctl configtest (IT should say ok, then go to next step)
```

4. Relode your apache server
```
sudo systemctl reload apache2
```

6. Obtaining an SSL Certificate
```
sudo certbot --apache (You have to answer some question here. Read carefully and answer)
```

7. Verifying Certbot Auto-Renewal
```
To make auto renewal process run ( sudo certbot renew --dry-run ) if you don't see any error, you are all set to go. And to check the certbot status please run ( sudo systemctl status certbot.timer )
```

7. Referance blog to install SSL with Let's Encrypt
```
https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-20-04
```