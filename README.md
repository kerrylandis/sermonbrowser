# WordPress Sermon Browser plugin update
I produced this in late 2018 out of necessity because so many churches started emailing me based on a solution I had provided in the WordPress forums. If you use the [WordPress Sermon Browser plugin](https://wordpress.org/plugins/sermon-browser/) that is no longer supported by the owner, this provides all the updated code in the frontend.php to allow for api.esv.org API v3 to work.

[Example output](https://www.cantonbiblechurch.org/sermons/no-rest-for-the-weary-under-the-sun/) of Bible verses being retrieved through the API and rendered on the page via a sortcode in WordPress: 

Please use the following steps to set this up as within your church website:

1. Go to https://api.esv.org/, create a login and then add your web application to generate a token ID. 
2. Once you get that ID, go to line 345 in the frontend.php file and just swap out the `###replaceWithToken###` with the 26 character alpha-numeric ID you create with https://api.esv.org/ when you register your website. The updated line should look something like this once you add your ID: `authorization: Token a1b2c3d4e5abcdefg1234567`
3. Once done, backup your frontend.php and replace it with this version and then test to confirm you are able to get the ESV verses.
