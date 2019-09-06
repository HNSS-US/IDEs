# To Do
### How To Migrate a MySQL Database Between Two Servers  
#### Using a SCP (Secure Copy)  

1. Perform a MySQL Dump  
   mysqldump -u root -p --opt [database name] > [database name].sql
   Example:
      $ sudo mysqldump -u root -p --opt cowrie > cowrie_frankfurt_de.sql
        Enter password: 

   
