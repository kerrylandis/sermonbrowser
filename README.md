# sermonbrowser
Updated code with esv.org V3 API call for WordPress Sermon Browser since this plugin is no longer supported by the owner.

This is an updated frontend.php file to allow for esv.org API v3 to work with the Sermon Browser plugin in Wordpress here:  https://wordpress.org/plugins/sermon-browser/

Please use the following steps to set this up as within your church website:

1. Go to https://api.esv.org/, create a login and then add your web application to generate a token ID. 
2. Once you get that ID, go to line 345 in the frontend.php file and just swap out the `###replaceWithToken###` with the 26 character alpha-numeric ID you create with https://api.esv.org/ when you register your website. The updated line should look something like this once you add your ID: `authorization: Token a1b2c3d4e5abcdefg1234567`
3. Once done, backup your frontend.php and replace it with this version and then test to confirm you are able to get the ESV verses.
