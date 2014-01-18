Configurare Virtual Host con MAMP
------------------------------------------------------------

1- Aggiungere nel file /etc/hosts

::

    127.0.0.1    clientA.local

2- Aggiungere in /Applications/MAMP/conf/apache/httpd.conf

::

    <VirtualHost *>
    DocumentRoot "/Users/YOU/sites/clientA/site"
    ServerName clientA.local
    </VirtualHost>

