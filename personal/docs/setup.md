1. Change config for Apache2 (or the other webservers' equivalents) in `sites-enabled` module (`/etc/apache2/sites-enabled/lamp-server.conf`) to contain:  
```
<VirtualHost *:80>
ServerAdmin webmaster@localhost
DocumentRoot /home/anthonytjuatja/educational-content-creator-platform
<Directory /home/anthonytjuatja/educational-content-creator-platform/>
    Options Indexes FollowSymLinks MultiViews
    AllowOverride All
    Require all granted
</Directory>
ErrorLog ${APACHE_LOG_DIR}/error.log
# Possible values include: debug, info, notice, warn, error, crit,
# alert, emerg.
LogLevel warn
CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```





