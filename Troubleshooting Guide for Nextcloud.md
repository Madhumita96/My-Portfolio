# Troubleshooting Guide for Nextcloud
## Introduction

Nextcloud is an open-source cloud storage and collaboration platform that allows users to store, share, and sync files securely. This guide provides troubleshooting steps for common issues users may encounter.

### Installation issues (Nextcloud installation fails)

**Symptom:** Installation does not complete, or errors appear during setup.Cause: Missing dependencies, incorrect permissions, or server configuration issues.
**Cause:** Missing dependencies, incorrect permissions, or server configuration issues.

# Resolution

1. Ensure that all required dependencies are installed:
   ```sh
   sudo apt update
   sudo apt install apache2 mariadb-server libapache2-mod-php php-gd php-mysql php-curl php-xml php-zip

2. Check file permissions:
   ```sh
   sudo chown -R www-data:www-data /var/www/nextcloud
   sudo chmod -R 755 /var/www/nextcloud

3. Verify that Apache or Nginx is running:
   ```sh
   sudo systemctl restart apache2

4. Review the installation logs:

   ```sh
   tail -f /var/log/apache2/error.log
   tail -f /var/log/nextcloud/nextcloud.log

## Login issues (Cannot log in to Nextcloud)

**Symptom:** The login page does not load, or credentials are rejected.
**Cause:** Incorrect database configuration, expired session, or browser cache issues.
**Resolution:** 
1. Clear the browser cache and cookies.
2. Verify database connectivity:
   ```sh
   sudo mysql -u root -p -e "USE nextcloud; SHOW TABLES;"
3. Reset the admin password:
   ```sh
   sudo -u www-data php /var/www/nextcloud/occ user:resetpassword admin
4. Check the Nextcloud logs:
   ```sh
   cat /var/www/nextcloud/data/nextcloud.log | tail -n 20
## File synchronization issues (Files are not syncing)

**Symptom:** Changes to files do not reflect across devices.
**Cause:** Sync client misconfiguration, connection issues, or permission errors.
**Resolution:**
1. Ensure that the Nextcloud client is running and connected.
2. Restart the Nextcloud sync client.
3. Verify server permissions:
   ```sh
   sudo -u www-data php /var/www/nextcloud/occ files:scan --all
4. Check sync logs in (for Linux)
   ```sh
   ~/.config/Nextcloud/nextcloud.log
   For (Windows)
   ```sh
   %APPDATA%\Nextcloud\nextcloud.log

