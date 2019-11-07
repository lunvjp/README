```
http://13.229.133.126/
```

```
sudo a2ensite example.com
sudo a2dissite example.com
sudo service apache2 restart
```

```
sudo usermod -a -G YOUR_USERNAME www-data
sudo setfacl -R -m u:YOUR_USERNAME:rwx /var/www/html
```

```
<VirtualHost *:80>
    ServerName payment.saigonstar.tk
    ServerAlias www.payment.saigonstar.tk
    ServerAdmin webmaster@payment.saigonstar.tk
    DocumentRoot /var/www/payment.saigonstar.tk/public_html

    <Directory /var/www/payment.saigonstar.tk/public_html>
        Options -Indexes +FollowSymLinks
        AllowOverride All
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/payment.saigonstar.tk-error.log
    CustomLog ${APACHE_LOG_DIR}/payment.saigonstar.tk-access.log combined
</VirtualHost>
```

* Create New FTP Account
```
sudo usermod -d /var/www/hoctaptaynguyen.tk/public_html/wordpress jack
```
> https://www.cyberciti.biz/faq/create-a-user-account-on-ubuntu-linux/
