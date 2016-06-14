# vagrant-wordpress
Fresh install of Wordpress with Vagrant+Ansible for development environment

1. Update the wp-config-sample.php and rename it to wp-config.php
2. Update the .htaccess-sample and rename it to .htaccess
3. Download Wordpress and unzip its content to the root
4. Update the roles/database/tasks/main.yml
  1. Update the # Create Database section
    - Change the databasename with the same in the wp-config.php
    - Remove the # from lines under this section
  2. If you created a user and password, Update the # User Password for Database access
    - Change the username, databasehost, password with the same in the wp-config.php
    - Remove the # from lines under this section
  3. If you have a db dump, Update # Copy database dump file to remote host and restore it to database
    - Copy the database backup to roles/database/files/
    - Change the db-backup with the name of the file copied in the last step
    - Remove the # from lines under this section

5. In the command shell launch Vagrant (vagrant up)
6. Access in the browser under the address: 10.11.12.13
7. Enjoy!
