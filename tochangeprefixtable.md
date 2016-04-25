To rename prefix from Wordpress database.
=========================================

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


This will return a lot of results, and you need to go one by one to change these lines.
------------------------------------------------------------------------

```
SELECT * FROM `namethatyouwant_options` WHERE `option_name` LIKE '%wp_%'
```