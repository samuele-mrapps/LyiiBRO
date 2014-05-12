Come fare il dump del database con mysql
----------------------------------------

::

    $ mysqldump -d -h localhost -u root -pmypassword mydatabase > dumpfile.sql 


Come importare il dump del database con mysql
----------------------------------------

::

    $ mysql -d -h localhost -u root -pmypassword mydatabase < dumpfile.sql 
