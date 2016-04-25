RENAME table `wp_commentmeta` TO `casarara_xthor_commentmeta`;
RENAME table `wp_comments` TO `casarara_xthor_comments`;
RENAME table `wp_links` TO `casarara_xthor_links`;
RENAME table `wp_options` TO `casarara_xthor_options`;
RENAME table `wp_postmeta` TO `casarara_xthor_postmeta`;
RENAME table `wp_posts` TO `casarara_xthor_posts`;
RENAME table `wp_terms` TO `casarara_xthor_terms`;
RENAME table `wp_term_relationships` TO `casarara_xthor_term_relationships`;
RENAME table `wp_term_taxonomy` TO `casarara_xthor_term_taxonomy`;
RENAME table `wp_usermeta` TO `casarara_xthor_usermeta`;
RENAME table `wp_users` TO `casarara_xthor_users`;

RENAME table `wp_termmeta` TO `casarara_xthor_termmeta`;
RENAME table `wp_wfBadLeechers` TO `casarara_xthor_wfBadLeechers`;
RENAME table `wp_wfBlockedIPLog` TO `casarara_xthor_wfBlockedIPLog`;
RENAME table `wp_wfBlocks` TO `casarara_xthor_wfBlocks`;
RENAME table `wp_wfBlocksAdv` TO `casarara_xthor_wfBlocksAdv`;
RENAME table `wp_wfConfig` TO `casarara_xthor_wfConfig`;
RENAME table `wp_wfCrawlers` TO `casarara_xthor_wfCrawlers`;
RENAME table `wp_wfFileMods` TO `casarara_xthor_wfFileMods`;
RENAME table `wp_wfHits` TO `casarara_xthor_wfHits`;
RENAME table `wp_wfHoover` TO `casarara_xthor_wfHoover`;
RENAME table `wp_wfIssues` TO `casarara_xthor_wfIssues`;
RENAME table `wp_wfLeechers` TO `casarara_xthor_wfLeechers`;
RENAME table `wp_wfLockedOut` TO `casarara_xthor_wfLockedOut`;
RENAME table `wp_wfLocs` TO `casarara_xthor_wfLocs`;
RENAME table `wp_wfLogins` TO `casarara_xthor_wfLogins`;
RENAME table `wp_wfNet404s` TO `casarara_xthor_wfNet404s`;
RENAME table `wp_wfReverseCache` TO `casarara_xthor_wfReverseCache`;
RENAME table `wp_wfScanners` TO `casarara_xthor_wfScanners`;
RENAME table `wp_wfStatus` TO `casarara_xthor_wfStatus`;
RENAME table `wp_wfThrottleLog` TO `casarara_xthor_wfThrottleLog`;
RENAME table `wp_wfVulnScanners` TO `casarara_xthor_wfVulnScanners`;


``This will return a lot of results, and you need to go one by one to change these lines.

SELECT * FROM `casarara_xthor_options` WHERE `option_name` LIKE '%wp_%'