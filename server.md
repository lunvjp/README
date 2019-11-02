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
