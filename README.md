# odoo_12_install
odoo 12 install script
# first of all we will update and upgrade the server system
sudo apt-get update && apt-get upgrade -y
# we need at this moment to install the html to pdf converter
#install wkhtmltopdf
sudo apt-get install xvfb libfontconfig wkhtmltopdf
# its time to install the database server
#install postgres
apt-get install postgresql -y
# finally let's go to odoo repository
#install from odoo repository
wget -O - https://nightly.odoo.com/odoo.key | apt-key add -
echo "deb http://nightly.odoo.com/12.0/nightly/deb/ ./" >> /etc/apt/sources.list.d/odoo.list
apt-get update && apt-get install odoo
################################################
#to start odoo
#sudo service odoo start
#to stop odoo
#sudo service odoo stop
#to restart odoo
#sudo service odoo restart
#to see status 
#service odoo status
################################################
