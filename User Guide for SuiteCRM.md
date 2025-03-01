# User Guide for SuiteCRM
## Introduction
SuiteCRM is an open-source customer relationship management (CRM) platform that helps businesses manage customer interactions, sales, and workflows. This guide provides step-by-step instructions on how to set up and use SuiteCRM effectively.
## 1. Get started
### 1.1 System requirements

Before you install SuiteCRM, make sure your system meets the following requirements:

- **Operating system:** Windows, macOS, or Linux

- **Web server:** Apache or Nginx

- **Database:** MySQL 5.7 or MariaDB 10+

- **PHP:** Version 7.4 or later

### 1.2 Install SuiteCRM
1. Download the latest version of SuiteCRM from the [official website](https://suitecrm.com/).
2. Upload the SuiteCRM files to your web server.
3. Set file permissions by running the following commands:

   ```sh
   sudo chown -R www-data:www-data /var/www/html/suitecrm
   sudo chmod -R 755 /var/www/html/suitecrm


4. In a web browser, go to http://yourdomain.com/suitecrm/install.php.
5. Follow the installation instructions to configure the database and admin account.

## 2. Navigate the interface

### 2.1 Dashboard overview

When you sign in, the SuiteCRM dashboard appears. The dashboard includes the following elements:

- **Navigation bar:** Provides quick access to key modules, such as Leads, Contacts, Accounts, and Reports.

- **Dashlets:** Displays recent activities, tasks, and key metrics.

- **User profile and settings:** Located in the upper-right corner.

### 2.2 Customize the dashboard

1. Select **Add Dashlet**.
2. Choose the widgets that you want to add.
3. Drag and drop dashlets to rearrange them.
4. Select Save and Convert.

## 4. Automate workflows

### 4.1 Create a workflow rule

1. In the navigation bar, select **Admin > Workflow**.
2. Select **Create Workflow**.
3. Define the conditions and actions. For example, configure a rule to send an email when a new lead is created.
4. Select **Save**.

## 5. Generate reports

### 5.1 Create a custom report

1. In the navigation bar, select **Reports**.
2. Select **Create Report**.
3. Choose the module, such as **Leads** or **Contacts**.
4. Define filters and display fields.
5. Select **Run Report**.

## 6. Troubleshoot common issues

### 6.1 Cannot sign in

**Symptom:** You are unable to sign in to SuiteCRM.
**Solution:** Verify that your credentials are correct. If necessary, select **Forgot Password** to reset your password.

### 6.2 Emails are not being sent

**Symptom:** Outgoing emails are not delivered.
**Solution:** Check email settings in **Admin > Email Configuration**. Ensure that SMTP settings are configured correctly.

Conclusion

This guide provides an overview of how to set up and use SuiteCRM. For advanced configurations, refer to the official [SuiteCRM Documentation](https://docs.suitecrm.com/).

