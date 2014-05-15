###<strong>Ansible playbook to add an Apache virtual host and ftp user. On Debian the config is added to /etc/apache2/sites-available/ while on RHEL is added to /etc/httpd/conf.d/. See apache_dir variable for that. Does reload apache. </strong> 

***
<strong>Usage:</strong> <br />
ansible-playbook -i inventory vhost.yml
***

<strong>Explanation for each variable:</strong>

site_url ==> Self explanatory. Do not use www. <br /> 
apache_port ==> Default 80. <br />
log_format ==> Apache log format. <br />

ftp_user ==> I hope I don't need to explain this. <br />
ftp_home ==> FTP home. Also vhost DocumentRoot. </br />
ftp_password ==> Same as above. <br />
ftp_shell ==> Pretty clear, default is /bin/false <br />

OS family variables:

apache_logs ==> Full path to apache log folder. <br />
apache_dir ==> Full path to apache configuration folder. <br />
apache_group ==> Apache group