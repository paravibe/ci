# Continious Integration
This is a collection of scripts that helps to build CI with GitLab and Jenkins.

## How to use
- You must have Ubuntu 14.04 or 12.04.
- Edit hosts file and replace IP address to desired one (you must have access to this machine via SSH).
- After that replace all CHANGE_ME placeholders in vars/vars.yml
- And start by ansible-playbook go.yml
- Enjoy!

## Variables
### vars/vars.yml
- **root_pass** - password for root user
- **root_comment** - root user name
- **sudo_user_name** - another sudouser
- **sudo_user_pass** - password for sudo user
- **sudo_user_comment** - name for sudo user

- **timezone** - timezone. E.g. "Europe/Kiev"

- **server_name** - This is used for creating nginx virtual host template. In most cases "{{ ansible_hostname }}" wors fine.

- **swapfile_location** - where to put swap. Default /swapfile.
- **swapfile_size** - swap size. E.g. 4G.

- **mysql_root_pass** - MySQL root password.

- **postfix_hostname** - hostname. E.g. example.com.
- **postfix_relayhost** - relayhost. For Google use '[smtp.gmail.com]:587'.
- **postfix_email** - email address which is used for sending mails. E.g. example@gmail.com.
- **postfix_email_pass** - password for your postfix_email.
- **postfix_notify_email** - this email is not used in the system and only used for notification of successful tasks complete.

- **ssl_certs_country** - certificate country. E.g. "UA".
- **ssl_certs_locality** - certificate city. E.g. "Lviv".
- **ssl_certs_organization** - certificate organization. E.g. "MyCorp".
- **ssl_certs_state** - certificate state.
- **ssl_certs_common_name** - certificate FQDN. For most cases "{{ ansible_fqdn }}" works fine.
- **ssl_certs_days** - expiration date in days. E.g. "1825".
- **ssl_storage_path** - where to store ssl certificate. Default to "/etc/nginx/ssl".

- **jenkins_web_url** - web url for jenkins. E.g. ci.example.com. Don't use http:// and trailing slash.
- **jenkins_user_name** - Jenkins root user name.
- **jenkins_user_pass** - Jenkins root password.
- **jenkins_user_mail** - Jenkins root email.
- **jenkins_pass_salt** - password salt string. E.g. secret.

- **gitlab_web_url** - GitLab web URL. E.g. git.example.com. Don't use http:// and trailing slash.
