# Bugs

## Web Cache Deception

This happens when a CDN or some caching mechanism caches a static file without checking is the content of that file is static or not

**https://www.youtube.com/watch?v=mroq9eHFOIU**

![enter image description here](Webcache.png)

## Conditions

 - The Web Application has to cache files with extensions disregarding any caching headers
 - When visiting a non existant page like localhost/home.php/notanactualfile.css the response of the request should server the content of home.php and has to be 200 OK
 - The victim has to be authenticated inorder to exfil session or csrf tokens
 - The Web Application should have a caching CDN like cloudflare,cloudfront or akami
