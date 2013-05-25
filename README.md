ubuntu-comment
==============
. The solution is

sudo /etc/init.d/apache2 stop
sudo /etc/init.d/mysql stop

And the restast with sudo //opt/lampp/lampp restart



t turns out that the solution is to stop all the services and solve the “Another daemon is already running” issue.

The commands i used to solve the issue are as follows:

sudo opt/lampp/lampp stop              
sudo /etc/init.d/apache2 stop    
sudo /etc/init.d/mysql stop

You can also type instead:

sudo service apache2 stop
sudo service mysql stop

After that, we start again the lampp services:

sudo opt/lampp/lampp start

Now, there must be no problems while opening:

http://localhost                  
http://localhost/phpmyadmin



----------------ssh enable on ubuntu------------------- 
mkdir ~/.ssh
chmod 700 ~/.ssh
ssh -i /path/to/key -vT git@github.com


Code:

ls -l `which sudo`

Code:

chmod 4755 `which sudo`

Code:

chown root:root `which sudo`

Ensure that the system complaining about the sudo command is using the host sudo, and not the client sudo.

Do something like:

Code:

updatedb && locate sudo

as root. See if you have multiple copies, and try to figure out which one is being invoked.
