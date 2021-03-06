# GaMerZ File Explorer

Enables you to browse a folder on the web like Windows Explorer. It has the ability to search for folders and files too.

## Installation

#### Config
* `$root_directory` - The absolute path of the folder that you want to show it's contents (without trailing slash).
 * Example: `/home/user/public_html/files`
* `$root_url` - The URL to that folder (without trailing slash).
 * Example: `http://yoursite.com/files`
* `$gfe_directory` - The absolute path of the folder you uploaded the files of GaMerZ File Explorer (without trailing slash).
 * Note: You Can Upload GaMerZ File Explorer Into The Same Folder As The Contents That You Want To Show.
 * Example: `/home/user/public_html/gfe`
* `$gfe_url` - The URL to that folder (without trailing slash).
 * Note: You can upload GaMerZ File Explorer into the same folder as the contents that you want to show.
 * Example: `http://yoursite.com/gfe`
* `$site_name` - Your site name
* `$root_filename` - Webserver directory index. Normally you do not need to change this.
* `$nice_url` - Search engine friendly URLs. See below.
 * Example Nice URL: `http://yoursite.com/gfe/browse/folder1/`.
 * Example Normal URL: `http://yoursite.com/gfe/index.php?dir=folder1`.
* `$can_search` - By setting to true, you allow users to search for files in GaMerZ File Explorer.
* `$default_sort_by` - Default sort field.
 * Values can be `name`, `size`, `type` or `date`.
* `$default_sort_order` - Default sort order.
 * Values can be `asc` or `desc`.

#### To Enable Search Engine Friendly URLs
* Upload '.htaccess' to the folder where you uploaded GaMerZ File Explorer.
* Open up '.htaccess' and replace all references of `/files/` to the folder path after your domain name of `$gfe_url`.
* Example: `$gfe_url = 'http://yoursite.com/gfe';`
* Your should replace `/files/` To `/gfe/`

#### Upload These Files To The Directory You Specify In `$gfe_directory`
* Folder: resources
* File: .htaccess (might be hidden)
* File: config.php
* File: functions.php
* File: index.php
* File: search.php
* File: settings.php
* File: view.php

## Changelog

#### Version 1.20 (01-02-2006)
* NEW: XHTML 1.1 Comptible Now

#### Version 1.20 Beta 3 (24-10-2006)
* FIXED: Error Displaying File Size More Than 2GB

#### Version 1.20 Beta 2 (25-03-2005)
* NEW: Added Default Sort Options
* NEW: HTML View Using IFRAME
* NEW: Added HTML View/HTML Source Option For HTML Files
* NEW: Added A JavaScript File Called javasript.js
* FIXED: Moved <style></style> Before </head>
* FIXED: Changed content-type To utf-8

#### Version 1.20 Beta (01-02-2005)
* NEW: Search Engine Now Implemented
* NEW: Added GB To The File Size
* NEW: .w3x Extensions Added
* FIXED: File Type Will Be 'Unknown' If File Type Is Not Registered In settings.php Instead Of Blank

#### Version 1.10 (01-12-2005)
* NEW: Now Support Nice URL Via Apache's mod_rewrite. User Can Choose To Enable/Disble Nice URL Option It In config.php
* NEW: Rewrote The Codes That Displays The Files And Folders, Now There Will Be No '/' In Front Of Any Folders Or Files
* NEW: settings.php Will Now Contain Most Of The Default Settings, So For Future Versions, You Do Not Need To Overwrite config.php Anymore
* NEW: Ability To Sort By Type
* NEW: Proper HTML Error Page
* NEW: `title=""` Being Added To Almost Every `<td>`
* NEW: favicon.ico Added
* NEW: .mdb|.mov|.msi|.ra|.rm|.tif|.wma|.wmv Extensions Added
* FIXED: Extension Not Showing When It Is In Upper Case
* FIXED: Files Listed In $ignore_files And $ignore_folders Will Now Be More Specified. If Ignore File Is 'test/test.htm', Only 'test.htm' In 'test' Folder Will Be Ignored Rather Than 'test.htm' Throughout All The Folders
* FIXED: No More Use Of PHP Short Tag
* FIXED: Unknown Or Undefined File Extension, The File Extension Image Will Now Be unknown.gif
* FIXED: Invalid Checking Of Directory in view.php
* FIXED: Grammer Mistakes For Singular And Pural
* FIXED: No Extension Given If There Is Spaces In The File Name That Is Being Downloaded

#### Version 1.00 (09-09-2005)
* NEW: Public Release Of GaMerZ File Explorer
