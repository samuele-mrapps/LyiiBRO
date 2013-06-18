Direttive apache per indicare la cartella root di un dominio
------------------------------------------------------------

::

    RewriteEngine on
    RewriteCond %{HTTP_HOST} ^(www.)?dominio.com$
    RewriteCond %{REQUEST_URI} !^/path/
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ /path/$1
    RewriteCond %{HTTP_HOST} ^(www.)?dominio.com$
    RewriteRule ^(/)?$ path/index.php [L]

Direttive apache per la cache
-----------------------------

::

    <IfModule mod_expires.c>
    ExpiresActive On
    ExpiresDefault "access plus 1 seconds"
    ExpiresByType text/html "access plus 1 seconds"
    ExpiresByType image/gif "access plus 120 minutes"
    ExpiresByType image/jpeg "access plus 120 minutes"
    ExpiresByType image/png "access plus 120 minutes"
    ExpiresByType text/css "access plus 60 minutes"
    ExpiresByType text/javascript "access plus 60 minutes"
    ExpiresByType application/x-javascript "access plus 60 minutes"
    ExpiresByType text/xml "access plus 60 minutes"
    </IfModule>
