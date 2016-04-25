How to Change the WordPress Database Prefix to Improve Security
===============================================================

Preparation
-----------

We recommend that you backup your WordPress Database before you perform anything suggested in this tutorial. It is important to keep daily backups of your site, we recommend BackupBuddy plugin for doing that. Next thing we recommend is that you redirect your visitors to a temporary maintenance page.

Change Table Prefix in wp-config.php
------------------------------------

Open your wp-config.php file which is located in your WordPress root directory. Change the table prefix line from wp_ to something else like this `namethatyouwant_`
So the line would look like this:

    $table_prefix  = 'namethatyouwant_';

> Note: You can only change it to numbers, letters, and underscores.

Change all Database Tables Name
-------------------------------

You need to access your database (most likely through phpMyAdmin), and then change the table names to the one we specified in wp-config.php file. If you are using the cPanel WordPress hosting, then you can find the phpMyAdmin link in your cPanel. Look at the image below:

![enter image description here](http://cdn2.wpbeginner.com/blogposts/phpmyadmin.gif)

There are a total of 11 default WordPress tables, so changing them manually would be pain.

![enter image description here](http://cdn3.wpbeginner.com/blogposts/sql.gif)

That’s why to make things faster, we have a SQL query that you can use.

```
RENAME table `wp_commentmeta` TO `namethatyouwant_commentmeta`;
RENAME table `wp_comments` TO `namethatyouwant_comments`;
RENAME table `wp_links` TO `namethatyouwant_links`;
RENAME table `wp_options` TO `namethatyouwant_options`;
RENAME table `wp_postmeta` TO `namethatyouwant_postmeta`;
RENAME table `wp_posts` TO `namethatyouwant_posts`;
RENAME table `wp_terms` TO `namethatyouwant_terms`;
RENAME table `wp_term_relationships` TO `namethatyouwant_term_relationships`;
RENAME table `wp_term_taxonomy` TO `namethatyouwant_term_taxonomy`;
RENAME table `wp_usermeta` TO `namethatyouwant_usermeta`;
RENAME table `wp_users` TO `namethatyouwant_users`;

RENAME table `wp_termmeta` TO `namethatyouwant_termmeta`;
RENAME table `wp_wfBadLeechers` TO `namethatyouwant_wfBadLeechers`;
RENAME table `wp_wfBlockedIPLog` TO `namethatyouwant_wfBlockedIPLog`;
RENAME table `wp_wfBlocks` TO `namethatyouwant_wfBlocks`;
RENAME table `wp_wfBlocksAdv` TO `namethatyouwant_wfBlocksAdv`;
RENAME table `wp_wfConfig` TO `namethatyouwant_wfConfig`;
RENAME table `wp_wfCrawlers` TO `namethatyouwant_wfCrawlers`;
RENAME table `wp_wfFileMods` TO `namethatyouwant_wfFileMods`;
RENAME table `wp_wfHits` TO `namethatyouwant_wfHits`;
RENAME table `wp_wfHoover` TO `namethatyouwant_wfHoover`;
RENAME table `wp_wfIssues` TO `namethatyouwant_wfIssues`;
RENAME table `wp_wfLeechers` TO `namethatyouwant_wfLeechers`;
RENAME table `wp_wfLockedOut` TO `namethatyouwant_wfLockedOut`;
RENAME table `wp_wfLocs` TO `namethatyouwant_wfLocs`;
RENAME table `wp_wfLogins` TO `namethatyouwant_wfLogins`;
RENAME table `wp_wfNet404s` TO `namethatyouwant_wfNet404s`;
RENAME table `wp_wfReverseCache` TO `namethatyouwant_wfReverseCache`;
RENAME table `wp_wfScanners` TO `namethatyouwant_wfScanners`;
RENAME table `wp_wfStatus` TO `namethatyouwant_wfStatus`;
RENAME table `wp_wfThrottleLog` TO `namethatyouwant_wfThrottleLog`;
RENAME table `wp_wfVulnScanners` TO `namethatyouwant_wfVulnScanners`;
```

You may have to add lines for other plugins that may add their own tables in the WordPress database. The idea is that you change all tables prefix to the one that you want.

The Options Table
-----------------

We need to search the options table for any other fields that is using wp_ as a prefix, so we can replace them. To ease up the process, use this query:

```
SELECT * FROM `namethatyouwant_options` WHERE `option_name` LIKE '%wp_%'
```

This will return a lot of results, and you need to go one by one to change these lines.

UserMeta Table
--------------

Next, we need to search the usermeta for all fields that is using wp_ as a prefix, so we can replace it. Use this SQL query for that:

    SELECT * FROM `namethatyouwant_usermeta` WHERE `meta_key` LIKE '%wp_%'

Number of entries may vary on how many plugins you are using and such. Just change everything that has wp_ to the new prefix.

Backup and Done
---------------

You are now ready to test the site. If you followed the above steps, then everything should be working fine. Now, you should make a new backup of your database just to be on the safe side.

> References: [enter link description
> here](http://www.wpbeginner.com/wp-tutorials/how-to-change-the-wordpress-database-prefix-to-improve-security/)