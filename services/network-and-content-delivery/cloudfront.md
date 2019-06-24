# Services | CloudFront

## General

* Key terminologies:

    * CDN - content delivery network

    * Edge Location - location where contents are cached; different from a Region and an AZ

    * Origin - origin of all files that CDN will distribute; can be S3 bucket, EC2 instance, ELB or Route 53

    * Distribution - name given to CDN which consists of a collection of Edge Locations

        * Web Distribution - used for websites

        * RTMP Distribution - used for media streaming using Adobe Flash Media

* Can be used to deliver your entire website, including dynamic, static, streaming and interactive content using a gobal network of edge locations

* Requests for content are automatically routed to the nearest edge location so content is delivered with the best possible performance

* Edge locations are not just READ only, you can write to them (eg., put object on Edge Location which is then replicated to the origin)

* Objects are cached for the life of TTL (time-to-live) - 24 days

* you can manually clear cached objects, but you will be charged

## Specifications

* Origin domain name - s3 bucket, on-premise URL

* Origin path - subdomain/folder inside bucket; default to blank

* Restrict Bucket Access - Yes then all requests to the Bucket is redirected to the CloudFront

* Origin Access Identity - user used when CloudFront is accessing S3

* Grant Read Permissions on Bucket - always select YES

* Path pattern - regex;

* Viewer Protocol Policy - HTTP and HTTPS, Redirect HTTP to HTTPS, HTTPS only

* Allowed HTTP Methods - GET, HEAD

* Maximum TTL - 365 days in seconds = 31536000

* Default TTL - 24 hours in second = 86400

* Restrict Viewer Access (Use Signed URLs or Signed Cookies) - Yes to set that only authenticated users can access files
