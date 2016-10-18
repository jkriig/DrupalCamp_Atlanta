# DrupalCamp_Atlanta

## Presentation Link
https://oie.gatech.edu/dcatl

## Notes:



### Offical Drupal HTTPS Infomation
[Link](https://www.drupal.org/https-information)

### HSTS Information
[Drupal Mod](https://www.drupal.org/project/hsts)

[Wikipedia](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)

## How-to:
-------------


##Updated htaccess to force non-www to https!
~~~~
RewriteEngine On
RewriteCond %{SERVER_PORT} !=443 [OR]
RewriteCond %{HTTP_HOST} ^www\.
RewriteRule ^(.*)$ https://pacific.gatech.edu/$1 [R=301,L]
~~~~

### Drupal Base URL in Settings.php
Set $base_url to SSL in settings.php.
~~~
$base_url = "https://www.example.com";
~~~


#alt htaccess
~~~~
RewriteEngine On
RewriteCond %{HTTPS} !=on
RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
~~~~





### Drupal CDN Module 
[Link](https://www.drupal.org/project/cdn)

[CDN Wikipedia](https://en.wikipedia.org/wiki/Content_delivery_network)

### CDN
[Keycdn.com](https://www.keycdn.com/?a=4189)

## How-to:
-------------
[Drupal CDN Guide by Keycdn.com](https://www.keycdn.com/support/drupal-cdn-integration/)

[IMCE Fix/Workaround for CDN](https://www.drupal.org/node/1585558)

[Touch Fix/Workaround](https://www.drupal.org/node/1740168)
