ConfigServer Firewall Installer
===============================

#### Description ####
Installs ConfigServer Firewall (CSF) and additional UI with credentials and port specified during install. Also installs shared SSL cert if needed (required for CSF UI) automatically and configures vhost accordingly. Tested and verified working on compatible distro's listed below.
<br><br>
###CentOS###
Will yum update & install these dependencies: ```sed openssl perl-Time-HiRes perl-libwww-perl perl-GDGraph perl-IO-Socket-SSL.noarch perl-Net-SSLeay perl-Net-LibIDN perl-IO-Socket-INET6 perl-Socket6 net-tools rsyslog mod_ssl```
<br><br>
Installs cert and key files @ /etc/pki/tls/certs (if chosing "y" to install ssl during install), mod_ssl, and edits /etc/httpd/conf.d/ssl.conf with locations.
<br><br>
###Ubuntu###
Will apt-get update & install these dependencies: ```apache2 sed openssl libio-socket-ssl-perl libcrypt-ssleay-perl libnet-libidn-perl libio-socket-inet6-perl libsocket6-perl```
<br><br>
Installs cert and key files @ /etc/apache2/ssl (if chosing "y" to install ssl during install), mod_ssl, and generates vhost @ /etc/apache2/sites-available/domain.com.conf with /var/www/html as root dir.
<br><br>
#### Compatability ####
CentOS 5/6/7
<br>
Ubuntu 12/14
<br><br>
#### Installation ####

```wget --no-check-certificate https://raw.github.com/stokes84/ConfigServer-Firewall-Installer/master/install.sh; bash install.sh; rm -f install.sh```
